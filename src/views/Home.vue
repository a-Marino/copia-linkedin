<template>
  <div class="home">
    <nav class="min-w-full py-3 fixed flex justify-center items-center space-x-5 h-10">
        <img src="@/assets/logo.png" alt="logo" class="h-9 w-auto">
        <img src="@/assets/icons/search.png" alt="search" class="h-5 w-auto">
        <div class="search-box hidden lg:block">
          <input type="text" class="search md:w-80" placeholder="Buscar">
        </div>
        <!-- NAV MOVIL -->
        <div class="flex space-x-7 md:hidden">
          <img src="@/assets/icons/home-button.png" alt="home" class="h-5 w-auto ">
          <img src="@/assets/icons/friends.png" alt="contacts" class="h-5 w-auto">
          <img src="@/assets/icons/suitcase.png" alt="jobs" class="h-5 w-auto">
          <img src="@/assets/icons/chat.png" alt="messages" class="h-5 w-auto">
          <img src="@/assets/icons/bell.png" alt="notifications" class="h-5 w-auto">
          <img src="@/assets/icons/user.png" alt="user" class="h-5 w-auto rounded-full hidden md:block">
        </div>
        <!-- NAV PC -->
        <div class="hidden md:flex space-x-3 flex-shrink-0">
          <div class="flex flex-col items-center px-3 py-1 active">
            <img src="@/assets/icons/home-button.png" alt="home" class="h-5 w-auto ">
            <span class="text-xs">Inicio</span>
          </div>
          <div class="flex flex-col items-center px-3 py-1">
            <img src="@/assets/icons/friends.png" alt="contacts" class="h-5 w-auto">
            <span class="text-xs">Mi red</span>
          </div>
          <div class="flex flex-col items-center px-3 py-1">
            <img src="@/assets/icons/suitcase.png" alt="jobs" class="h-5 w-auto">
            <span class="text-xs">Empleos</span>
          </div>
          <div class="flex flex-col items-center px-3 py-1">
            <img src="@/assets/icons/chat.png" alt="messages" class="h-5 w-auto">
            <span class="text-xs">Mensajes</span>
          </div>
          <div class="flex flex-col items-center px-3 py-1">
            <img src="@/assets/icons/bell.png" alt="notifications" class="h-5 w-auto">
            <span class="text-xs">Notificaciones</span>
          </div>
          <div class="flex flex-col items-center px-3 py-1 relative">
            <button id="user">
              <img src="@/assets/icons/user.png" alt="user" class="h-5 w-auto rounded-full -mb-1">
              <span class="text-xs">Yo</span>
            </button>
            <!-- POP UP USER -->
            <div class="box-user flex flex-col p-3 absolute top-14 right-0" id="box-user">
              <div class="flex space-x-2">
                <img src="@/assets/icons/user.png" alt="user" class="h-14 w-auto rounded-full">
                <div class="flex flex-col">
                  <h2 class="font-semibold">Andres Marino</h2>
                  <h3 class="text-sm">Front End Dev | JavaScript | VueJs | HTML | CSS | TailwindCSS</h3>
                </div>
              </div>
              <a href="#" class="btn-seeProfile self-center my-2 text-sm font-semibold">Ver perfil</a>
              <div class="flex flex-col space-y-2">
                <h2 class="font-semibold">Cuenta</h2>
                <span class="text-sm">Ajustes y privacidad</span>
                <span class="text-sm">Ayuda</span>
                <span class="text-sm">Idioma</span>
              </div>
              <div class="flex flex-col space-y-2 mt-2">
                <h2 class="font-semibold">Gestionar</h2>
                <span class="text-sm">Publicaciones y actividad</span>
                <span class="text-sm">Cuenta de anuncios de empleo</span>
              </div>
              <span class="text-sm mt-4">Cerrar sesion</span>
            </div>
          </div>
        </div>
        <div class="hidden lg:flex space-x-3 flex-shrink-0">
          <div class="flex flex-col items-center px-3 py-1">
            <img src="@/assets/icons/grid.png" alt="user" class="h-5 w-auto">
            <span class="text-xs">Para negocios</span>
          </div>
        </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Home',
  mounted() {
    const userBtn = document.querySelector('#user');
    const boxUser = document.querySelector('#box-user')

    userBtn.addEventListener('click', ()=> {
      boxUser.classList.toggle('hidden');
    })
  }
}
</script>

<style scoped>
nav {
  height: 60px;
  overflow: visible;
}

span {
  color: rgb(121, 121, 121);
  cursor: pointer;
}

span:hover {
  color: black;
}
.search {
  border: 0;
  border-radius: 5px;
  padding: 10px;
  height: 35px;
}

.active {
  border-bottom: 2px solid black;
}

.box-user {
  border: 1px solid rgb(192, 192, 192);
  border-radius: 10px;
  width: 250px;
  height: 380px;
  
  background: #fff;
  float: left;
}

.btn-seeProfile {
  border: 1px solid #0A66C2;
  width: 100%;
  text-align: center;
  border-radius: 20px;
  color: #0A66C2;
}

.btn-seeProfile:hover {
  border: 2px solid #0A66C2;
  
}
</style>
