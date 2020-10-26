<template>
<div class="container-fluid m-0 p-0">
    <div id="home-page" class="full-height p-4">
        <div class="container pt-3">
            <div class="row pb-5">
                <div class="col-lg-6 pt-4 my-auto">
                    <div class="text-center mb-3 d-block d-lg-none">
                        <h1 class="display-3">{{ title }}</h1>
                        <h3>Доставка грузов в Кыргызстан. <br> Любой сложности из любой точки мира</h3>
                    </div>
                    <img id="iphone-img" src="../assets/iphone.png" class="img-fluig">

                </div>
                <div class="col-lg-6 my-auto pt-4">
                    <div class="text-center mb-3 d-none d-lg-block">
                        <h1 class="display-3">{{ title }}</h1>
                        <h3>Доставка грузов в Кыргызстан. <br> Любой сложности из любой точки мира</h3>
                    </div>

                    <div class="border p-3 p-md-5 bg-white rounded shadow">
                        <h2>Запуск уже скоро</h2>
                        <form @submit.prevent="addEmail(email)">
                            <div class="form-group">
                                <label for="emailSignup">Откройте свой аккаунт прямо сейчас! Мы свяжемся с вами, когда сервис запуститься.</label>
                                <input v-model="email"
                                        type="email" 
                                        id="emailSignup" 
                                        placeholder="Введите вашу почту"
                                        class="form-control"
                                >
                                <small id="emailHelp" class="form-text text-muted">Ваша приватность - наш приоритет!</small>
                                <button type="submit" class="btn btn-success mt-3">Присоединяйтесь к списку ожидания</button>
                                <div class="mt-4">
                                    <p class="m-0">
                                        {{ message }}
                                    </p>
                                </div>
                            </div>
                        </form>
                    </div>

                    <div id="available" class="p-2">
                        <h4 class="text-center mb-2 mt-3 text-light">
                            Дата запуска
                        </h4>
                        <div class="row">
                            <div class="col my-auto">
                                <img src="../assets/app-store.png" class="float-right img-fluid app_store_img">
                            </div>
                                <div class="col my-auto">
                                <img src="../assets/google-play.png" class="float-left img-fluid app_store_img">
                            </div>

                        </div>
                    </div>
                </div>

            </div>
        </div>

    </div>

    <div id="about" class="bg-light p-3 p-md-5">
        <div class="row">
            <div class="col-lg">
                <img src="../assets/icons/boxes.png" height="120" class="m-4">
                <h5 class="ml-md-4 mr-mf-4">
                    Хранение на складах.
                    Molestiae et vel voluptas. Sequi quod eveniet aut culpa soluta distinctio quam et. 
                    Sequi eum nesciunt voluptatum consequatur. Corporis repudiandae deserunt vitae impedit quis recusandae. 
                </h5>
            </div>

            <div class="col-lg">
                <img src="../assets/icons/cash-on-delivery.png" height="120" class="m-4">
                <h5 class="ml-md-4 mr-mf-4">
                    Самый бюджетный.
                    Molestiae et vel voluptas. Sequi quod eveniet aut culpa soluta distinctio quam et.
                    Sequi eum nesciunt voluptatum consequatur. Corporis repudiandae deserunt vitae impedit quis recusandae. 
                </h5>
            </div>

            <div class="col-lg">
                <img src="../assets/icons/planet.png" height="120" class="m-4">
                <h5 class="ml-md-4 mr-mf-4">
                    Оптимальный. 
                    Molestiae et vel voluptas. Sequi quod eveniet aut culpa soluta distinctio quam et.
                    Sequi eum nesciunt voluptatum consequatur. Corporis repudiandae deserunt vitae impedit quis recusandae.
                </h5>
            </div>
        </div>

    </div>

    <div id="contact" class="p-4">
        <div class="row justify-content-center mt-3 mb-3">

        <div class="col-lg-4">
          <h2>Свяжитесь с нами</h2>
          <p>Заполните форму ниже</p>

          <form>
            <div class="form-group text-left ">
              <input 
                     type="email"
                     class="form-control"
                     placeholder="Введите адрес почты"
                     >
              <textarea 
                        class="form-control mt-3"
                        placeholder="Введите ваше сообщение"
                        rows="5"
              ></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Отправить</button>
          </form>
        </div>
      </div>

    </div>

    <div id="footer" class="bg-primary p-4">
        <footer class="text-light p-4">
            <a href="#" class="text-warning">Политика Конфиденциальности</a>
            <br>
            <small>&copy; 2020, logistic_solutions.kg</small>
      </footer>

    </div>

</div>
</template>

<script>
import { Auth } from '@/firebase/auth.js'

export default {
  data () {
      return {
          title: 'Logistic Solutions',
          email: '',
          message: '',
      }
    },
    
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#home-page {
    background-color: #92D2F2;
    background: url('../assets/main.jpg') no-repeat center center;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
}

#about {
    min-height: 40vh;
}

#iphone-img {
    max-height: 80vh;
}

#contact {
    background-color: #57AEAF;
}

.app_store_img {
    max-height: 80px;
}

</style>
