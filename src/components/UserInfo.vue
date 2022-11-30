<template>
    <div class="cp-userinfo-c">
        <el-button class="info-btn" text>
            <el-avatar shape="square" :size="30" fit="fits.fill" :src="url" />
            <div class="username-c">{{ usernmae }}</div>
            <div class="updown-c">
                <el-icon size="20"><DCaret /></el-icon>
            </div>
            <div class="show-c">
                <el-button text  ><el-icon><DArrowLeft /></el-icon></el-button>
                
            </div>
        </el-button>
    </div>
</template>

<script setup lang="ts">
import { reactive, toRefs } from 'vue';

const state = reactive({
    fits: ['fill', 'contain', 'cover', 'none', 'scale-down'],
    url: 'https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg',
    usernmae: "陶善忠",
})

const { fits, url, usernmae } = toRefs(state)
</script>

<style lang="scss" scoped>
@font-face {
    font-family: alibaba2;
    src: url("../assets/font/0BpYovnY7SJHxvWroPJ-C.woff2");

}

.cp-userinfo-c {

    .info-btn {
        font-family: alibaba2;
        color: #b8b8b8;
        width: 212px;
        height: 60px;
        // display: flex;
        // flex-direction:row;
        // justify-content: space-around;
.el-avatar{
    margin-left: 15px;
}
        .username-c {
                    margin-left: 10px;
                    margin-right: 10px;
                    font-size: 20px;
                }
                .show-c{
                    margin-left: 35px;
                    margin-right: 10px;
                    
                }
                
    }
}
</style>