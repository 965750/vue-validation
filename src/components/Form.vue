<template>
    <div class="formCont">
        <div class="bg"></div>
        <div><span class="formBtn formActive">Login</span><span class="formBtn">sign Up</span></div>
        <form method="POST" action="">
            <fieldset>
                <label class="inpTitle" for="email">email</label>
                <input class="inpPost" type="text" name="email" id="email">
                <label class="inpTitle" for="password">password</label>
                <input class="inpPost" type="password" name="password" id="password">
                <div class="checkboxCont">
                    <label class="inpTitle" for="remember">Remember me</label>
                    <div class="squaredFour">
                        <input type="checkbox" value="None" id="remember" name="check" checked />
                        <label for="remember"></label>
                    </div>
                </div>
                <input class="inpSubmit" type="submit" value="login">
            </fieldset>
        </form>
        <div class="errorCont"><span class="errorText">Just a simple error</span></div>
    </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      msg: ""
    };
  }
};
</script>

<style lang="scss" scoped>
.formCont {
  width: 400px;
  height: 340px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 10px;
  box-sizing: border-box;
  background: rgba(165, 203, 69, 0.76);
  border-radius: 15px;
  box-shadow: 0 0 5px #333;
  .errorCont {
    border-bottom: 2px solid #d6e7aa;
    margin-top: 10px;
    text-align: center;
    height: 20px;
    .errorText {
      color: crimson;
    }
  }
  fieldset {
    border: none;
    background: rgba(165, 203, 69, 0.342);
    margin: 20px auto 10px;
    border-radius: 5px;
  }
  .bg {
    background: url("../assets/background.jpg") center;
    position: absolute;
    top: 0px;
    left: 0px;
    z-index: -1;
    width: 100%;
    height: 100%;
    opacity: 0.25;
    border-radius: 15px;
  }
  .formBtn {
    text-transform: uppercase;
    color: #858585;
    font-weight: 700;
    margin: 0px 7px;
    font-size: 17px;
    transition: all 0.1s;
    &:hover {
      color: #fff;
      cursor: pointer;
    }
  }
  .formActive {
    color: #fff;
    border-bottom: 3px solid rgb(112, 240, 0);
  }
  .inpPost {
    width: 100%;
    height: 40px;
    margin: auto;
    display: block;
    border-radius: 20px;
    border: none;
    padding: 5px 5px 5px 10px;
    box-sizing: border-box;
    background: rgb(214, 231, 170);
    margin: 0px 0px 15px;
    outline: none;
    opacity: 0.7;
    color: #3a3a3a;
    font-size: 17px;
    &:focus {
      border: 1px solid rgb(112, 240, 0);
      background: rgb(228, 240, 199);
    }
  }
  .inpPost:nth-child(4) {
    margin-bottom: 10px;
  }
  .inpSubmit {
    @extend .inpPost;
    color: #3a3a3a;
    font-weight: 700;
    font-size: 20px;
    text-transform: uppercase;
    opacity: 0.9;
    background: rgb(112, 240, 0);
    margin: 20px 0px 5px;
    transition: all 0.1s;
    &:hover {
      cursor: pointer;
      background: rgb(100, 223, 0);
      color: #ffffff;
    }
  }
  .inpTitle {
    color: #3a3a3a;
    text-transform: uppercase;
    font-weight: 700;
    font-size: 14px;
    padding-left: 10px;
  }
  .checkboxCont {
    display: flex;
    .squaredFour {
      width: 16px;
      position: relative;
      margin: 0px 0px 0px 10px;
      label {
        width: 16px;
        height: 16px;
        cursor: pointer;
        position: absolute;
        top: 0;
        left: 0;
        background: #a7e400;
        border-radius: 4px;
        box-shadow: inset 0px 1px 1px #fff, 0px 1px 3px rgba(0, 0, 0, 0.5);
        &:after {
          content: "";
          width: 7px;
          height: 4px;
          position: absolute;
          top: 4px;
          left: 3px;
          border: 3px solid #333;
          border-top: none;
          border-right: none;
          background: transparent;
          opacity: 0;
          transform: rotate(-45deg);
        }
        &:hover::after {
          opacity: 0;
        }
      }
      input[type="checkbox"] {
        visibility: hidden;
        &:checked + label:after {
          opacity: 1;
        }
      }
    }
  }
}
</style>
