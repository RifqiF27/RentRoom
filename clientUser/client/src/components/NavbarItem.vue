<template>
  <!--======Nav======-->
  <nav class="navbar navbar-expand-xl navbar-dark bg-dark fixed-top">
    <a href="/" class="navbar-brand p-2 m-auto">
      <img src="../assets/logo.png" alt="logo" />
      Rent<b>Room</b>
    </a>
    <button
      type="button"
      class="navbar-toggler"
      data-toggle="collapse"
      data-target="#navbarCollapse"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <!-- Collection of nav links, forms, and other content for toggling -->
    <div
      id="navbarCollapse"
      class="collapse navbar-collapse justify-content-start"
    >
      <div class="navbar-nav ml-auto">
        <div class="nav-item dropdown">
          <a
            href=""
            data-toggle="dropdown"
            class="nav-item nav-link dropdown-toggle user-action"
          >
            <img
              src="https://source.boringavatars.com/beam/40"
              class="avatar"
              alt="Avatar"
            />
            {{ username }}
            <b class="caret"></b>
          </a>
          <div class="dropdown-menu">
            <a href="" class="dropdown-item" @click="$router.push('/login')"
              ><i class="fa fa-user-o"></i>Sign In</a
            >
            <div class="divider dropdown-divider"></div>
            <a href="#" class="dropdown-item" @click="doLogout()"
              ><i class="material-icons">&#xE8AC;</i> Logout</a
            >
           
          </div>
        </div>
        <a href="#" class="nav-item nav-link" @click="$router.push('/')"
          ><i class="fa fa-home"></i>Home</a
        >
        <a
          href="#"
          class="nav-item nav-link"
          @click="$router.push('/bookmarks')"
          ><i class="fa fa-bookmark" aria-hidden="true"></i>Bookmark</a
        >
        <!-- <a href="#" class="nav-item nav-link"><i class="fa fa-users"></i><span>Team</span></a>
          <a href="#" class="nav-item nav-link"><i class="fa fa-pie-chart"></i><span>Reports</span></a>
          <a href="#" class="nav-item nav-link"><i class="fa fa-briefcase"></i><span>Careers</span></a>
          <a href="#" class="nav-item nav-link"><i class="fa fa-envelope"></i><span>Messages</span></a>		
          <a href="#" class="nav-item nav-link"><i class="fa fa-bell"></i><span>Notifications</span></a> -->
      </div>
    </div>
  </nav>
</template>

<script>
import { mapActions, mapWritableState } from "pinia";
import { useCounterStore } from "../stores/counter";
export default {
  methods: {
    // props: ['username'],
    // data() {
    //   return {
    //     username: "",
    //   };
    // },
    ...mapActions(useCounterStore, [
      "logoutHandler",
      "loginHandler",
      "registerHandler",
    ]),
    doLogout() {
      this.logoutHandler();
    },
  },
  computed: {
    ...mapWritableState(useCounterStore, ["username"]),
  },
  created() {
    this.username = localStorage.username;
  },
  // updated() {
  //   console.log(this.username)
  // },
  // watch: {
  //   ['$route'](){
  //     console.log(localStorage.username);
  //     // if(localStorage.username){
  //       this.username = localStorage.username;
  //       console.log(this.username, '<<>>')
  //     // }else{
  //     //   this.username = ''
  //     // }
  //   }
  // }
};
</script>

<style></style>
