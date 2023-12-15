<template>
  <div class="login-wrap">
  <div class="login-html">
    <input id="tab-1" type="radio" name="tab" class="sign-in" checked><label for="tab-1" class="tab">Sign In</label>
    <input id="tab-2" type="radio" name="tab" class="sign-up"><label for="tab-2" class="tab">Sign Up</label>
    <div class="login-form">
      <div class="sign-in-htm">
        <div class="group">
          <label for="user" class="label">Username</label>
          <input id="user" type="text" class="input">
        </div>
        <div class="group">
          <label for="pass" class="label">Password</label>
          <input id="pass" type="password" class="input" data-type="password">
        </div>
        <div class="group">
          <input id="check" type="checkbox" class="check" checked>
          <label for="check"><span class="icon"></span> Keep me Signed in</label>
        </div>
        <div class="group">
          <input type="submit" class="button" value="Sign In">
        </div>
        <div class="hr"></div>
        <div class="foot-lnk">
          <a href="#forgot">Forgot Password?</a>
        </div>
      </div>
      <div class="sign-up-htm">
        <div class="group">
          <label for="user" class="label">Username</label>
          <input id="user" type="text" class="input">
        </div>
        <div class="group">
          <label for="pass" class="label">Password</label>
          <input id="pass" type="password" class="input" data-type="password">
        </div>
        <div class="group">
          <label for="pass" class="label">Repeat Password</label>
          <input id="pass" type="password" class="input" data-type="password">
        </div>
        <div class="group">
          <label for="pass" class="label">Email Address</label>
          <input id="pass" type="text" class="input">
        </div>
        <div class="group">
          <input type="submit" class="button" value="Sign Up">
        </div>
        <div class="hr"></div>
        <div class="foot-lnk">
          <label for="tab-1">Already Member?</label>
        </div>
      </div>
    </div>
  </div>
</div>
</template>
<script setup>
// export default {
//     name: 'LoginView',
//     data () {
//         return {
//             user: {
//                 email: '',
//                 password: ''
//             }
//         }
//     },
//     methods: {
//         login () {
//             this.$auth.login({
//                 params: {
//                     email: this.user.email,
//                     password: this.user.password
//                 },
//                 success: () => {
//                     this.$router.push({name: 'home'})
//                 },
//                 error: (err) => {
//                     console.log(err)
//                 }
//             })
//         }
//     }
// }
</script>

<style scoped>
  
  body{
	margin:0;
	color:#79797c;
	background:#c8c8c8;
	font:600 16px/18px 'Open Sans',sans-serif;
}
*,:after,:before{box-sizing:border-box}
.clearfix:after,.clearfix:before{content:'';display:table}
.clearfix:after{clear:both;display:block}
a{color:inherit;text-decoration:none}

.login-wrap{
	width:100%;
	margin:auto;
	max-width:525px;
	min-height:670px;
	position:relative;

	/* background:url(https://raw.githubusercontent.com/khadkamhn/day-01-login-form/master/img/bg.jpg) no-repeat center; */
	/* box-shadow:0 12px 15px 0 rgba(255, 255, 255, 0.24),10px 17px 50px 0 rgba(0,0,0,.19); */
 
}
.login-html {
  width: 100%;
  height: 100%;
  position: absolute;
  padding: 90px 70px 50px 70px;
  background-color: rgba(10, 10, 10, 0.336);
  backdrop-filter: blur(10px); /* Increase the blur value */
  -webkit-backdrop-filter: blur(10px); /* Increase the blur value */
  border: 1px solid rgba(175, 174, 174, 0.568);
}
.login-html .sign-in-htm,
.login-html .sign-up-htm{
	inset:0;
  /* top:0;
	left:0;
	right:0;
	bottom:0; */
	position:absolute;
	transform:rotateY(180deg);
	backface-visibility:hidden;
	transition:all .4s linear;
  
}
.login-html .sign-in,
.login-html .sign-up,
.login-form .group .check{
	display:none;
	color: #4b4b4b;
 
}
.login-html .tab,
.login-form .group .label,
.login-form .group .button{
	text-transform:uppercase;
  color: #6a6a6d;
}
.login-html .tab{
	font-size:22px;
	margin-right:15px;
	padding-bottom:5px;
	margin:0 15px 10px 0;
	display:inline-block;
	border-bottom:2px solid transparent;
  cursor: pointer;
}
.login-html .sign-in:checked + .tab,
.login-html .sign-up:checked + .tab{
  color:#ffffff;
  /*  */
  border-color:#0019f7;
}
.login-form{
	min-height:345px;
	position:relative;
	perspective:1000px;
	transform-style:preserve-3d;
}
.login-form .group{
	margin-bottom:15px;
}
.login-form .group .label,
.login-form .group .input,
.login-form .group .button{
	width:100%;
	color:#fffcfc;
	display:block;
}
.login-form .group .input,
.login-form .group .button{
	border:none;
  height: 50px;
	padding:15px 20px;
	border-radius:30px;
	background:#ffffff62;
}
.login-form .group input[data-type="password"]{
  -webkit-text-security: circle;
}
.login-form .group .label{
	color:#ffffff;
	font-size:12px;
}
.login-form .group .button{
	background:rgba(128, 132, 134, 0.514);
  width: 35%;
  margin-left: 30%;
}
.login-form .group .button:hover{
  background:#1132ee;
}
.login-form .group label .icon{
	width:15px;
	height:15px;
	border-radius:2px;
	position:relative;
	display:inline-block;
	background:rgb(255, 255, 255);
}
.login-form .group label .icon:before,
.login-form .group label .icon:after{
	content:'';
	width:10px;
	height:2px;
	background:#fffefe;
	position:absolute;
	transition:all .2s ease-in-out 0s;
}
.login-form .group label .icon:before{
	left:3px;
	width:5px;
	bottom:6px;
	transform:scale(0) rotate(0);
}
.login-form .group label .icon:after{
	top:6px;
	right:0;
	transform:scale(0) rotate(0);
}
.login-form .group .check:checked + label{
	color:#ffffff;
}
.login-form .group .check:checked + label .icon{
	background:#081fee;
}
.login-form .group .check:checked + label .icon:before{
	transform:scale(1) rotate(45deg);
}
.login-form .group .check:checked + label .icon:after{
	transform:scale(1) rotate(-45deg);
}
.login-html .sign-in:checked + .tab + .sign-up + .tab + .login-form .sign-in-htm{
	transform:rotate(0);
}
.login-html .sign-up:checked + .tab + .login-form .sign-up-htm{
	transform:rotate(0);
}

.hr{
	height:2px;
	margin:60px 0 50px 0;
	background:rgb(255, 255, 255);
}
.foot-lnk{
	text-align:center;
  margin-top: -40px;
  color: #a5a4a4b2;
  
}

</style>