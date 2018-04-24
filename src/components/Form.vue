<template>
    <div class="formCont">
        <div class="bg"></div>
        <div><span class="formBtn formActive">sign In</span><span class="formBtn">sign Up</span></div>
        <form method="POST" action="">
            <fieldset>
                <label class="inpTitle" for="email">email</label>
                <input class="inpPost" type="text" name="email" id="email">
                <label class="inpTitle" for="password">password</label>
                <input class="inpPost" type="password" name="password" id="password">
                <label class="inpTitle" for="remember">Remember me</label>
                <input type="checkbox" name="remember" id="remember">
                <input class="inpSubmit" type="submit" value="login">
            </fieldset>
        </form>
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
    .formCont{
        width: 400px;
        height: 300px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        padding: 10px;
        box-sizing: border-box; 
        background: #A6CB45;
        
        .bg{
            background: url('../assets/background.jpg') center;
            position: absolute;
            top: 0px;
            left: 0px;
            z-index: -1;
            width: 100%;
            height: 100%; 
            opacity: .2;
        }
        .formBtn{
            text-transform: uppercase;
            color: #858585;
            font-weight: 700;
            margin: 0px 7px;
            font-size: 17px;
            transition: all .1s;
            &:hover{
                color:#fff;
                cursor: pointer;
            }
        }
        .formActive{
            color: #fff;
            border-bottom: 3px solid green;
        }
        .inpPost{
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
            opacity: .7;
        }
        .inpSubmit{
            @extend .inpPost;
            color: #fff;
            font-size: 20px;
            text-transform: uppercase;
            opacity: .9
        }
        .inpTitle{
            color: #3a3a3a;
            text-transform: uppercase;
            font-weight: 700;
            font-size: 14px;
            padding-left: 10px;
        }
    }
</style>
