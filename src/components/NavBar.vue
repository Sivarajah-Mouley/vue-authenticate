<template>
    <header class="header">
      <a href="#" class="logo">Logo</a>
      <nav class="navbar">
        <div>
          <RouterLink to="/" active-class="active">Home</RouterLink>
          <RouterLink to="/about" active-class="active">About</RouterLink>
          <RouterLink to="/login" active-class="active">Login</RouterLink>
        </div>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: 'NavBar',
  }
  </script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap');
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
/* body {
    min-height: 100vh;
    background: url('background.jpg') no-repeat;
    background-size: cover;
    background-position: center;
} */
.header {
    position: fixed;
    top: 0;
    z-index: 1;
    left: 0;
    width: 100%;
    padding: 20px 50px;
    background: rgba(255, 255, 255, .1);
    display: flex;
    justify-content: space-between;
    align-items: center;
    backdrop-filter: blur(10px);
    border-bottom: 2px solid rgba(255, 255, 255, .2);
}
.header::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, .4), transparent);
    transition: .5s;
}
.header:hover::before {
    left: 100%;
}
.logo {
    color: #fff;
    font-size: 25px;
    text-decoration: none;
    font-weight: 600;
    cursor: default;
}
.navbar a {
    color: #fff;
    font-size: 18px;
    text-decoration: none;
    margin-left: 35px;
    transition: .3s;
}
/* .navbar a:active {
  color: red;
} */
.router-link-exact-active {
    color: red !important;
    font-weight: 520;
}

/* .router-link-active {
  color: red !important;
} */
.navbar a:hover {
    color: #f00;
}
</style>
