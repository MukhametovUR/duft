<template>
  <div class="wrp">
    <img src="../assets/logo.svg" alt="logo" class="logo" />
    <form
      class="form-signup"
      action=""
      method="post"
      name="form"
      @submit.prevent
    >
      <div class="header">
        <h2 class="title">РЕГИСТРАЦИЯ</h2>

        <div class="add-photo">
          <span class="add-photo__text">Добавить фотографию</span>
          <img src="../assets/circle.svg" alt="add-photo" />

          <v-btn class="btn-plus" fab dark small absolute bottom right>
            <v-icon>mdi-plus</v-icon>
          </v-btn>
        </div>
      </div>
      <div class="form-signup__item">
        <MyLabel for="firstname">Имя:*</MyLabel>
        <MyInput type="text" name="firstname" placeholder="Константин" />
      </div>
      <div class="form-signup__item">
        <MyLabel for="fullname">Фамилия:*</MyLabel>
        <MyInput
          type="text"
          name="lastname"
          placeholder="Константинопольский"
        />
      </div>
      <div class="form-signup__item">
        <MyLabel for="cityname">Город:*</MyLabel>
        <MyInput type="text" name="cityname" placeholder="Москва" />
      </div>
      <div class="form-signup__item">
        <MyLabel for="email">Email:*</MyLabel>
        <MyInput type="email" name="email" placeholder="" />
      </div>
      <div class="form-signup__item">
        <MyLabel for="email">Дата рождения:*</MyLabel>
        <MyInput type="date" name="date" placeholder="01.01.1980" />
      </div>
      <div class="check-gender form-signup__item">
        <MyLabel for="">Пол:</MyLabel>

        <div>
          <input type="radio" checked="checked" />
          <MyLabel for="gender">Мужской</MyLabel>
        </div>
        <div>
          <input type="radio" />
          <MyLabel for="gender">Женский</MyLabel>
        </div>
      </div>
      <div class="form-signup__item">
        <MyLabel for="innemployer">ИНН работодателя:*</MyLabel>

        <MyInput
          type="number"
          name="innemployer"
          placeholder="1010101010101010"
        />
      </div>
      <div class="form-signup__item">
        <MyLabel for="employer">Работодатель:</MyLabel>
        <MyInput
          type="text"
          name="employer"
          placeholder="ООО “Константин и Ко”"
        />
      </div>
      <div class="add-photo__mini">
        <MyLabel for="photo">Добавить фотографию:</MyLabel>
        <img src="../assets/circle.svg" alt="photo__mini" class="photo__mini" />

        <v-btn class="btn-plus" fab dark small absolute right bottom>
          <v-icon>mdi-pen</v-icon>
        </v-btn>
      </div>
      <MyButton type="submit" class="btn">Зарегистрироваться</MyButton>
    </form>
  </div>
</template>
<script>
import MyLabel from "../components/MyLabel.vue";
import MyInput from "../components/MyInput.vue";
import MyButton from "../components/MyButton.vue";

export default {
  name: "FormSignUp",

  components: {
    MyInput,
    MyLabel,
    MyButton,
  },
};
</script>
<style scoped>
* {
  background: url("/src/assets/fon.svg");
}
.wrp {
  background-color: rgba(2, 0, 17, 1);
}
.logo {
  display: block;
  margin: 60px auto;
}
.header {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 100%;
  background: #172144;
}
.title {
  color: #fff;
  display: flex;
  align-items: flex-end;
  background: #172144;
}
.check-gender {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  color: #fff;
  flex-grow: 1;
}
.add-photo {
  color: #fff;
  position: relative;
}
.add-photo img {
  background: #172144;
}
.add-photo__text {
  font-weight: 400;
  font-size: 15px;
  line-height: 16px;
  opacity: 50%;
  bottom: 50%;
  display: flex;
  justify-content: center;
  position: absolute;
  text-align: center;
}

.add-photo__mini {
  color: #fff;
  position: relative;
}
.photo__mini {
  height: 100px;
}
.form-signup {
  display: flex;
  flex-wrap: wrap;
  margin: auto auto;
  justify-content: space-between;
  position: absolute;
  max-width: 700px;
  font-size: 16px;
  font-weight: 300;
  padding: 50px 90px;
  position: relative;
  -webkit-transition: all 0.5s ease;
  transition: all 0.5s ease;
  background: #172144;
}
.form-signup__item {
  margin: 15px 0;
  background: #172144;
}
.btn-plus {
  background: linear-gradient(90deg, #ff00b1 0%, #b423c1 100%);
  box-shadow: 0px 0px 10px #d70e93;
  top: 100px;
}
.add-photo__mini {
  display: none;
}
@media (max-width: 768px) {
  .logo {
    margin: 15px auto;
  }
  .form-signup {
    max-width: 400px;
  }
  .add-photo {
    display: none;
  }
  .add-photo__mini {
    display: flex;
    flex-direction: column;
    background: #172144;
  }
  .add-photo__mini img {
    background: #172144;
  }
}
</style>