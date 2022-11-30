<template>
    <div>
        <el-button text class="noteheader-btn-c">
            <el-button link @click="downf" class="noteheader-down-c">
                <el-icon size="20" v-show="!down">
                    <Folder />
                </el-icon>
                <el-icon size="20" v-show="down">
                    <FolderOpened />
                </el-icon>
            </el-button>

            <div class="noteheader-headertxt-c">
                {{ headertxt }}
            </div>
            <el-button link class="noteheader-moretool-c">
                <el-icon size="18">
                    <MoreFilled />
                </el-icon>
            </el-button>
            <el-button link class="noteheader-plustool-c">
                <el-icon size="18">
                    <CirclePlus />
                </el-icon>
            </el-button>

        </el-button>
        <ul v-if="down" v-for="downlist in downlists">
            <BookItems :headertxt="downlist" ></BookItems>
        </ul>
    </div>
</template>

<script setup lang="ts">
import { reactive, toRefs } from 'vue';
import BookItems from './BookItems.vue';


//标题 下含笔记本名 下拉显示
const props = defineProps({
    headertxt: String,
    downlists: Array<String>,
})
const state = reactive({
    down: false,
    headertxt: props.headertxt,
    downlists: props.downlists,
})
function downf() {
    state.down = !state.down;
}
const { down, headertxt, downlists } = toRefs(state)


</script>

<style lang='scss' scoped>
.noteheader-btn-c {
    font-family: alibaba2;
    color: #b8b8b8;
    width: 224px;
    height: 40px;
    display: flex;
    flex-direction: row;
    justify-content: left;

    .noteheader-down-c {
        width: 10px;
        margin-right: 10px;
    }

    .noteheader-headertxt-c {
        width: 170px;
        overflow: hidden;
        margin-right: 16px;
        text-align: left;
        font-size: 18px;
        

    }

     .noteheader-moretool-c {
        margin-right: 0px;
        display: none;
    }

    .noteheader-plustool-c {
        margin-left: 1px;
        display: none;
    }

}
.noteheader-btn-c:hover .noteheader-moretool-c {
    display:block;
}
.noteheader-btn-c:hover .noteheader-plustool-c{
    display:block;
}
.noteheader-btn-c:hover .noteheader-headertxt-c {
    width: 120px;
}
</style>