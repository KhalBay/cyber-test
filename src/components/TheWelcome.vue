<script setup lang="ts">
import {useRouter} from "vue-router";

const router = useRouter()

const goToTask = async () => {
  await router.push('/posts')
}
const imgLinks = {
  first: "https://sun9-14.userapi.com/impg/kBuZ8sEHBZ5Qoa8qpf4IuVtFXDDFYZxDrBsHZw/3EprioXv3j8.jpg?size=1215x2160&quality=95&sign=ad3fb5aa2ccddbfbbe442739fb6ce432&type=album",
  second: "https://sun9-52.userapi.com/impg/5kMo4p4TBSB-FgqSnwdU9cQ8WJpxOBCgZ3jdog/bLChMbRX9dU.jpg?size=607x1080&quality=95&sign=b77b2ce3962e55748a4cc1e27fc13814&type=album"
}
</script>

<template>
  <div class="welcome">
    <h1>🤚 Привет, меня зовут Егор, а это мое тестовое задание</h1>
    <div class="welcome__section">
      <div class="welcome__side">
        <h2>У меня есть четыре кота, вот один из них</h2>
        <img :src="imgLinks.first" alt="Должен быть я" class="welcome__img">
      </div>
      <div class="welcome__side revert">
        <h2>Здесь я плаваю с женой на сапе</h2>
        <img :src="imgLinks.second" alt="Должен быть я снова" class="welcome__img">
      </div>
    </div>
    <h3>Это я всё к чему: люблю животных и активный отдых 🎉</h3>
    <h3>Приятно познакомиться, давайте перейдем к тому, что я сделал</h3>
    <button @click="goToTask">Задание (тык)💻</button>
    <h5>Пишите <a href="https://telegram.me/KhalBay7">по любому вопросу </a> в Telegram</h5>
  </div>
</template>

<style lang="scss" scoped>
.welcome {
  text-align: center;

  &__section {
    display: flex;
    gap: 20px;
  }

  &__side {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    flex: 1 1 0;

    &.revert {
      align-items: flex-start;
    }
  }

  &__img {
    width: 212px;
    height: 378px;
  }
}
</style>