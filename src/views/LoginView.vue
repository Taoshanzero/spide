
<template>
    <div class="indextop">
        <el-container>
            <el-header class="header-parent-class">
                <div class="header-div-class">
                    <div class="header-left-class">
                        <SparkingIcon />
                        <p id="top-logo">sparking</p>
                        <p id="top-logotext">花火</p>
                    </div>
                    <div class="header-right-class">
                        <div class="header-right-a-class">下载</div>
                        <div class="header-right-a-class">进入官网</div>
                        <div class="header-right-a-class">帮助中心</div>
                    </div>
                </div>
            </el-header>
            <el-main class="main-parent-class">
                <div class="main-login-class">
                    <div class="main-welcome-class">
                        <p class="main-welcome-font">欢迎使用sparking</p>

                    </div>
                    <div class="main-loginginput-class">
                        <div class="main-account-class">
                            <el-input placeholder="请输入邮箱" clearable />
                        </div>
                        <div class="main-password-class">
                            <el-input type="password" placeholder="请输入密码" show-password />
                        </div>
                        <div class="main-tips-class ">
                            <div class="main-tips-font">忘记密码？</div>
                        </div>
                        <div class="main-loginbtn-class">
                            <el-button color="#b8b8b8" size="large">登录</el-button>
                        </div>
                    </div>
                    <div class="main-loginconnect-class">
                        <div class="main-full-class"></div>
                        <div class="main-captcha-class">
                            <el-button color="#b8b8b8" size="large">验证码</el-button>
                        </div>
                        <div class="main-register-class">
                            <div class="main-register-font">注册账号</div>
                        </div>
                        <div class="main-anther-class">
                            <div class="main-another-font">---------------其他登录方式---------------</div>
                        </div>
                        <div class="main-gitee-class">
                            <IconGitee/>
                        </div>
                    </div>
                </div>
            </el-main>
            <el-footer class="main-tips-font">
                
                    <div>&copy;lsa19030陶善忠</div>
                
            </el-footer>
        </el-container>
    </div>
</template>


<script setup lang="ts">
import SparkingIcon from "../components/icons/IconSpark.vue"
import IconGitee from "../components/icons/IconGitee.vue"
</script>

<style lang="scss">
.indextop {
    height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: #171717;

    .el-container {
        width: 100%;
        min-height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        .el-header {

            height: 68px;

            .header-div-class {

                margin: 32px 48px 0px 48px;
                height: 36px;
                display: flex;
                flex-wrap: nowrap;
                justify-content: space-between;

                .header-left-class {

                    width: 200px;
                    display: flex;
                    flex-wrap: nowrap;
                    justify-content: space-evenly;
                }

                .header-right-class {

                    width: 200px;
                    display: flex;
                    flex-wrap: nowrap;
                    justify-content: space-between;
                }
            }
        }

        .el-main {

            height: 100%;
            overflow: hidden;
            display: flex;
            justify-content: center;

            .main-login-class {

                padding-top: 150px;
                width: 400px;
                height: 550px;

                .main-welcome-class {

                    height: 64px;
                    margin-bottom: 23px;

                }

                .main-loginginput-class {
                    // background-color: rgb(98, 161, 115);
                    height: 230px;

                    .main-account-class {
                        height: 50px;
                        margin-bottom: 20px;

                        .el-input {
                            height: 50px;
                        }
                    }

                    .main-password-class {
                        margin-bottom: 10px;

                        .el-input {
                            height: 50px;
                            size: larger;
                        }
                    }

                    .main-tips-class {}

                    .main-loginbtn-class {
                        margin-top: 28px;

                        .el-button {
                            width: 100%;
                            height: 50px;

                        }
                    }

                }

                .main-loginconnect-class {

                    height: 230px;

                    .main-full-class {
                        height: 1px;
                    }

                    .main-captcha-class {

                        margin-top: 30px;

                        .el-button {
                            width: 100%;
                            height: 50px;

                        }
                    }

                    .main-register-class {
                        margin-top: 12px;
                        display: flex;
                        justify-content: center;
                    }

                    .main-anther-class {
                        margin-top: 32px;
                        display: flex;
                        justify-content: center;
                    }
                    .main-gitee-class{
                        margin-top: 10px;
                        display: flex;
                        justify-content: center;
                    }
                }
            }
        }
    }

    .el-footer {

        display: flex;
        height: 42px;
        width: 100%;
        justify-content: center;
        .div{
            font-family: alibaba2;
    font-weight: 100;
    font-size: 18px;
    color: #b8b8b863;
    
        }
    }

}



@font-face {
    font-family: alibaba2;
    src: url("../assets/font/0BpYovnY7SJHxvWroPJ-C.woff2");
}

#top-logo {
    font-family: alibaba2;
    font-weight: 400;
    font-size: 22px;
    line-height: 28px;
    color: #b8b8b8;
}

#top-logotext {
    font-family: alibaba2;
    font-weight: 100;
    font-size: 22px;
    line-height: 28px;
    color: #b8b8b8;
}

.header-right-a-class {
    font-family: alibaba2;
    font-weight: 500;
    font-size: 16px;
    line-height: 28px;
    color: #b8b8b8;
}

.main-welcome-font {
    font-family: alibaba2;
    font-weight: 600;
    font-size: 40px;
    color: #b8b8b8;
    text-align: center;
}

.main-tips-font {
    font-family: alibaba2;
    font-weight: 100;
    font-size: 3px;
    color: #b8b8b8;
    text-align: right;
}

.main-register-font {
    font-family: alibaba2;
    font-weight: 100;
    font-size: 15px;
    color: #b8b8b8;
    text-align: right;
}
.main-another-font {
    font-family: alibaba2;
    font-weight: 100;
    font-size: 15px;
    color: #b8b8b863;
    text-align: right;
}
</style>