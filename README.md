<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>KBpassword</title>
  <style>
    html {
  height: 100%;
}
body {
  margin:0;
  padding:0;
  font-family: sans-serif;
  background: linear-gradient(#141e30, #243b55);
}

.login-box {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  padding: 40px;
  transform: translate(-50%, -50%);
  background: rgba(0,0,0,.5);
  box-sizing: border-box;
  box-shadow: 0 15px 25px rgba(0,0,0,.6);
  border-radius: 10px;
}

.login-box h2 {
  margin: 0 0 30px;
  padding: 0;
  color: #fff;
  text-align: center;
}

.login-box .user-box {
  position: relative;
}

.login-box .user-box input {
  width: 100%;
  padding: 10px 0;
  font-size: 16px;
  color: #fff;
  margin-bottom: 30px;
  border: none;
  border-bottom: 1px solid #fff;
  outline: none;
  background: transparent;
}
.login-box .user-box label {
  position: absolute;
  top:0;
  left: 0;
  padding: 10px 0;
  font-size: 16px;
  color: #fff;
  pointer-events: none;
  transition: .5s;
}

.login-box .user-box input:focus ~ label,
.login-box .user-box input:valid ~ label {
  top: -20px;
  left: 0;
  color: #03e9f4;
  font-size: 12px;
}

.login-box form a {
  position: relative;
  display: inline-block;
  padding: 10px 20px;
  color: #03e9f4;
  font-size: 16px;
  text-decoration: none;
  text-transform: uppercase;
  overflow: hidden;
  transition: .5s;
  margin-top: 40px;
  letter-spacing: 4px;
    outline:none;
    cursor: pointer;
}

.login-box a:hover {
  background: #03e9f4;
  color: #fff;
  border-radius: 5px;
  box-shadow: 0 0 5px #03e9f4,
              0 0 25px #03e9f4,
              0 0 50px #03e9f4,
              0 0 100px #03e9f4;
    outline:none;
}

.login-box a span {
  position: absolute;
  display: block;
  outline:none;
}

.login-box a span:nth-child(1) {
  top: 0;
  left: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent, #03e9f4);
  animation: btn-anim1 1s linear infinite;
}

@keyframes btn-anim1 {
  0% {
    left: -100%;
  }
  50%,100% {
    left: 100%;
  }
}

.login-box a span:nth-child(2) {
  top: -100%;
  right: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(180deg, transparent, #03e9f4);
  animation: btn-anim2 1s linear infinite;
  animation-delay: .25s
}

@keyframes btn-anim2 {
  0% {
    top: -100%;
  }
  50%,100% {
    top: 100%;
  }
}

.login-box a span:nth-child(3) {
  bottom: 0;
  right: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(270deg, transparent, #03e9f4);
  animation: btn-anim3 1s linear infinite;
  animation-delay: .5s
}

@keyframes btn-anim3 {
  0% {
    right: -100%;
  }
  50%,100% {
    right: 100%;
  }
}

.login-box a span:nth-child(4) {
  bottom: -100%;
  left: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(360deg, transparent, #03e9f4);
  animation: btn-anim4 1s linear infinite;
  animation-delay: .75s
}

@keyframes btn-anim4 {
  0% {
    bottom: -100%;
  }
  50%,100% {
    bottom: 100%;
  }
}
#message {
  font-size: 18px;
  color: #ff6666; /* Dark Fiery Red */
  font-weight: bold;
  animation: shimmer 2s infinite;
}

@keyframes shimmer {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}

  </style>
</head>
<body>
  <div class="login-box">
    <h2>Khata book </h2>
    <h2>Login</h2>
    <form>
      <div class="user-box">
        <input id="inputUserID" type="text" name="" required="">
        <label>Username</label>
      </div>
      
      <div class="user-box">
        <input  id="inputPassword" type="password" name="" required="">
        <label>Password</label>
      </div>
      <a onclick="checkPassword()" >
        <span></span>
        <span></span>
        <span></span>
        <span></span>
        Submit
      </a>
    </form>
    <p id="message"></p>
  </div>
  <script>
    // User IDs and passwords for different users
    const MahaarshiID = "Maharshi";
    const PrathamID = "PrathamID";
    const JayID = "Jay";
    const ChaitanyaID = "Chaitanya";
    const RoshanID = "Roshan";
    const PriyanshID = "Priyansh";

    // Passwords corresponding to user IDs
    const Maharshipsw = "MAharshi@JAVA";
    const Prathampsw = "mr.patel0407";
    const Jaypsw = "Gjay@3022";
    const Chaitanyapsw = "756818@gk";
    const Roshanpsw = "R.k1305";
    const Priyanshpsw = "Pri(47)FromCA@";

    function checkPassword() {
      const userID = document.getElementById("inputUserID").value;
      const password = document.getElementById("inputPassword").value;

      // Check the user ID and password for each user
      if (userID === MahaarshiID && password === Maharshipsw) {
        // Redirect to the desired URL for this user
        window.location.href = "file:///C:/xampp/htdocs/p/KB!MB.html";
      } else if (userID === PrathamID && password === Prathampsw) {
        // Redirect to the desired URL for this user
        window.location.href = "file:///C:/xampp/htdocs/p/KB!PP.html";
      } else if (userID === JayID && password === Jaypsw) {
        // Redirect to the desired URL for this user
        window.location.href = "file:///C:/xampp/htdocs/p/KB!GJ.html";
      } else if (userID === ChaitanyaID && password === Chaitanyapsw) {
        // Redirect to the desired URL for this user
        window.location.href = "file:///C:/xampp/htdocs/p/KB!CP.html";
      } else if (userID === RoshanID && password === Roshanpsw) {
        // Redirect to the desired URL for this user
        window.location.href = "file:///C:/xampp/htdocs/p/KB!RK.html";
      } else if (userID === PriyanshID && password === Priyanshpsw) {
        // Redirect to the desired URL for this user
        window.location.href = "file:///C:/xampp/htdocs/p/KB!SP.html";
      } else {
        // If none of the cases match, show an error message
        document.getElementById("message").textContent = "Invalid username or password.";
      }
    }
  </script>
</body>
</html>
