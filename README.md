<!DOCTYPE html>
<html>
<style>
/* Full-width input fields */
input[type=text], input[type=password] {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    box-sizing: border-box;
}

/* Set a style for all buttons */
button {
  width:200px;
  height:35px;
  display:block;
  font-family:Arial, "Helvetica", sans-serif;
  font-size:16px;
  font-weight:bold;
  color:#fff;
  text-decoration:none;
  text-transform:uppercase;
  text-align:center;
  text-shadow:1px 1px 0px #37a69b;
  padding-top:6px;
  margin: 29px 0 0 29px;
  position:relative;
  cursor:pointer;
  border: none;  
  background-color: #b380ff;
  background-image: linear-gradient(top,#ffb380,#ffb380);
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  border-bottom-left-radius:5px;
  box-shadow: inset 0px 1px 0px #2ab7ec, 0px 5px 0px 0px #ffb380, 0px 10px 5px #ffb380;
}

.btnposition {
    margin: 10px 0 0 60px;
}


/* Extra styles for the cancel button */
.cancelbtn {
    width: auto;
    margin: 0px 200px;
    padding: 10px 18px;
    background-color: #004d99;
}

/* Center the image and position the close button */
.imgcontainer {
    text-align: center;
    margin: 24px 0 12px 0;
    position: relative;
}

img.avatar {
    width: 40%;
    border-radius: 50%;
}

.container {
    padding: 16px;
}

span.psw {
    float: right;
    padding-top: 16px;
}

/* The Modal (background) */
.modal, .modal2 {
    display: none; /* Hidden by default */
    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgb(0,0,0); /* Fallback color */
    background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
    padding-top: 60px;
}

/* Modal Content/Box */
.modal-content {
    background-color: #fefefe;
    margin: 5% auto 15% auto; /* 5% from the top, 15% from the bottom and centered */
    border: 1px solid #888;
    width: 350px; /* Could be more or less, depending on screen size */
    bac
}

/* The Close Button (x) */
.close {
    position: absolute;
    right: 25px;
    top: 0;
    color: #000;
    font-size: 35px;
    font-weight: bold;
}




.select-style {
    border: 1px solid #ccc;
    width: 200px;
    text-align: center;
    border-radius: 3px;
    overflow: hidden;
    background: #fafafa url("img/icon-select.png") no-repeat 90% 50%;
}

.select-style select {
    padding: 5px 8px;
    width: 130%;
    border: none;
    box-shadow: none;
    background: transparent;
    background-image: none;
    -webkit-appearance: none;
}

.select-style select:focus {
    outline: none;
}




.close:hover,
.close:focus {
    color: red;
    cursor: pointer;
}

/* Add Zoom Animation */
.animate {
    -webkit-animation: animatezoom 0.6s;
    animation: animatezoom 0.6s
}

@-webkit-keyframes animatezoom {
    from {-webkit-transform: scale(0)} 
    to {-webkit-transform: scale(1)}
}
    
@keyframes animatezoom {
    from {transform: scale(0)} 
    to {transform: scale(1)}
}

/* Change styles for span and cancel button on extra small screens */
@media screen and (max-width: 300px) {
    span.psw {
       display: block;
       float: none;
    }
    .cancelbtn {
       width: 100%;
    }
}
.p2{
  border: 2px solid #ffb380;
  border-radius: 15px;
  background-color: #660066;
  height: 165px;
  width: 260px;
}
.po{
  border: 2px solid #809fff;
  border-radius: 5px;
  height: 40px;
  box-shadow: inset 0px 1px 0px #2ab7ec, 0px 5px 0px 0px #ff8080, 0px 10px 5px #ff8080;
}
.leftcenter {
  height: 380px;
  margin: 95px 200px;
  width: 340px;
}

</style>
<head><title> Sign-In & Sign-Up</title></head>
<body>

<h2>Pieyyouel Blizzard Entertainment.</h2>
<p class="po"></p>
<div class="leftcenter">
<p class="p2">
<button onclick="document.getElementById('forlog').style.display='block'" style="width:200px;" >Login</button>
<button onclick="document.getElementById('forreg').style.display='block'" style="width:200px;" >Register</button></p>
</div><p class="po"></p>


<div id="forlog" class="modal">
  
  <form name="signin" class="modal-content animate" onsubmit="return tosignin();">
    <div class="imgcontainer">
      <span onclick="document.getElementById('forlog').style.display='none'" class="close" title="Close Modal">&times;</span>
    </div>

    <div class="container"></br>

      <input type="text" name="Eid" id="emailid" placeholder="Email - example@gmail.com" required>
      <input type="password" name="pass1" id="pass1" placeholder="Password" required>  
      <button type="signin" name="signin" class="btnposition">Sign-In</button>

    </div>

    <div class="container" style="background-color:#f1f1f1">
      <button type="button" onclick="document.getElementById('forlog').style.display='none'" class="cancelbtn">Cancel</button>
    </div>
  </form>
</div>


<div id="forreg" class="modal2">
  <form name="signup" class="modal-content animate" onsubmit="return tovalidate();">

    <div class="imgcontainer">
      <span onclick="document.getElementById('forreg').style.display='none'" class="close" title="Close Modal">&times;</span>
    </div>




    <div class="container">
      </br>
      <input type="text" name="Uid" id="userid" placeholder="Username" required>
      <input type="text" name="Eid" id="emailid" placeholder="Email - example@gmail.com" required>
      <input type="text" name="Cnum" id="contactnumber" placeholder="+63947201003" required>
      <center><label id="gender">Gender:</label> 
      <input type="radio" name="ml" value="Male" /><span>Male</span> 
      <input type="radio" name="fm" value="Female" /><span>Female</span>
      <div class="select-style">
      <select name="country">
      <option selected="" value="Default">Select Country</option>  
      <option value="PH">Philippines</option> 
      <option value="IR">Ireland</option>  
      <option value="JPN">Japan</option>  
      <option value="KR">Korea</option>  
      <option value="RS">Russia</option>  
      <option value="US">USA</option>  
      </select></div></center></br>
      <label><b>Password:</b></label>
      <input type="password" name="pass1" id="pass1" placeholder="Password" required>
      <label><b>Password Confirmation:</b></label>
      <input type="password" name="pass2" id="pass2" placeholder="Password Confirmation" required>
      

      <button type="signup" name="signup" class="btnposition">SignUp</button>



    </div>






    <div class="container" style="background-color:#f1f1f1">
      <button type="button" onclick="document.getElementById('forreg').style.display='none'" class="cancelbtn">Cancel</button>
    </div>

  </form>
</div>





<script>
// Get the modal
var modal = document.getElementById('forlog');
var modal2 = document.getElementById('forreg');

// When the user clicks anywhere outside of the modal, close it
window.onclick = function(event) {
    if (event.target == modal ) {
        modal.style.display = "none";
    }
    if (event.target == modal2) {
        modal2.style.display = "none";
    }
}


      function tosignin(){
          var Eid = document.signin.Eid;
          var Pass1 = document.signin.pass1;
          if(Eid_SignIn(Eid)){

          }
          if(Pass_SignIn(Pass1)){

          }
      }

      function Eid_SignIn(p){
              if((p.value)=="Pieyyouel@gmail.com"){
                  return true;
              }
              else{
                  p.focus();
                  return false;

              }
        }
      function Pass_SignIn(p){
              if((p.value)=="Pieyyouel"){
                  alert("Signing In!")
                  return true;
              }
              else{
                  p.focus();
              }
        }





        function tovalidate(){  
          var Uid = document.signup.Uid;
          var Eid = document.signup.Eid;
          var Cnum = document.signup.Cnum;
          var mgender = document.signup.ml;
          var fgender = document.signup.fm;
          var Sctry = document.signup.country;
          var Pass1 = document.signup.pass1;
          var Pass2 = document.signup.pass2;
          if(Uid_Validation(Uid,5,12)){

          }
          if(Eid_Validation(Eid)){

          }
          if(Cnum_Validation(Cnum)){

          }
          if(Gender_Validation(mgender,fgender)){

          }
          if(CountrySelect(Sctry)){

          }
          if(Pass_Confirm_Validation(Pass1,Pass2)){

          }
          
          else{
            return false;
          }
        }

        function Uid_Validation(uid,x,y){
            var uid_len = uid.value.length;
            alert(uid.value);
        }

        function Eid_Validation(eid){
            var atpos = eid.value.indexOf("@");
              var dotpos = eid.value.lastIndexOf(".");
              if (atpos<1 || dotpos<atpos+2 || dotpos+2>=eid.length) {
                  alert("Not a valid e-mail address");
                  eid.focus();
                  return false;
              }
           
        }

        function Cnum_Validation(a){
          var phoneno = /^\d{11}$/;  
              if(a.value.match(phoneno))  
                 {  
                   alert(a.value);
                   return true;  
                 }  
               else  
                 {  
                   alert("Not a valid Phone Number");  
                   a.focus();
                   return false;  
                 }  
        }

        function Gender_Validation(x,y){
            if(x.checked==false && y.checked==false ) {
                alert("You must select your gender.");
                return false;
            }   
        }

        function CountrySelect(s){
                if(s.value == "Default")  
                  {  
                      alert('Select country from the given list.');  
                      s.focus();  
                      return false;  
                  }  
                  else  
                  {  
                      return true;  
                  }  
        }

        function Pass_Confirm_Validation(x,y){
        if((x.value.length > 6) && (y.value.length > 6)){
            if(x.value == y.value){
                alert("Welcome @ WW");
                return true;
            }
          }
            else{
                x.focus();
                alert("Please re-enter password and atleast 8 character long.")
                return false;
            }
        }




</script>

</body>
</html>
