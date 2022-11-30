
<template>
    <div class="common-layout">
        <el-container>
            <el-aside width="240px">
                <div class="aside-user-c">
                    <UserInfoVue />
                </div>
                <div class="aside-toolbar-c">
                    <el-button text>
                        <el-icon size="20">
                            <Search />
                        </el-icon>
                    </el-button>
                    <el-button text>
                        <el-icon size="20">
                            <Bell />
                        </el-icon>
                    </el-button>
                    <el-button text>
                        <el-icon size="20">
                            <Upload />
                        </el-icon>
                    </el-button>
                    <el-button text>
                        <el-icon size="20">
                            <Setting />
                        </el-icon>
                    </el-button>
                </div>
                <span class="aside-deliver-c"></span>

                <div class="aside-notes-c">
                    <div class="aside-tips-c">
                        <p class="aside-tips-f">个人页面</p>
                        <el-button text>
                            <el-icon>
                                <Plus />
                            </el-icon>
                        </el-button>
                    </div>
                    <el-scrollbar><ul class="aside-notetable-c" v-for="downlist in downlists">
                        <NoteItems headertxt="sda" :downlists="downlist"></NoteItems>
                    </ul></el-scrollbar>
                    
                </div>
            </el-aside>
            <el-container>
                <el-header>Header</el-header>
                <el-main>Main</el-main>
            </el-container>
        </el-container>
    </div>
</template>



<script setup lang="ts">
import UserInfoVue from '@/components/UserInfo.vue';
import NoteItems from '@/components/NoteItems.vue';
import { reactive, toRefs } from 'vue';
const state = reactive({
    downlists: [['hahah', 'sada', 'sada'
        , 'sada', 'sada', 'sada', 'sada', 'sada', 'sada', 'sada', 'sada', 'sada', 'sada', 'sada', 'sada', 'sada', 'sada'], ['dsf', 'asdsa']],
})
const { downlists } = toRefs(state)
</script>

<style lang="scss" scoped>
.el-container {
    font-family: alibaba2;
    color: #b8b8b8;
    height: 100vh;
    overflow: hidden;
    width: 100vw;
    background-color: #171717;

    .el-aside {
        background-color: #1e1e1e;
        display: flex;
        flex-direction: column;

        .aside-user-c {
            height: 62px;
            padding: 10px;

        }

        .aside-toolbar-c {
            height: 48px;
            padding: 10px;
            display: flex;
            flex-direction: row;
            justify-content: center;

            .el-button {
                height: 50px;
                width: 50px;
                margin: 4px;
            }
        }

        .aside-deliver-c {
            border-width: 1px 0px 0px 0px;
            margin-left: 16px;
            margin-right: 16px;
            border-style: solid;
            border-top-color: #2e2e2e;
        }

        .aside-notes-c {
            margin-top: 16px;
            

            .aside-tips-c {
                height: 38px;
                display: flex;
                flex-direction: row;



                .aside-tips-f {
                    margin-left: 10px;
                    font-size: small;
                    margin-top: 5px;
                }

                .el-button {
                    margin-left: auto;
                    margin-right: 10px;

                    height: 30px;
                    width: 30px;
                }
            }

            .el-scrollbar {
                margin-left: 8px;
                margin-right: 8px;
                height: 600px;
                overflow-x: hidden;
                
            }
        }
    }
}

@font-face {
    font-family: alibaba2;
    src: url("../assets/font/0BpYovnY7SJHxvWroPJ-C.woff2");
}
</style>