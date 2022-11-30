<template>
    <div>
        <el-button text class="noteheader-btn-c">
            <el-button link  class="noteheader-down-c">
                <el-icon size="18">
                    <Notebook />
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

        </el-button>
    </div>
</template>

<script setup lang="ts">import { reactive, toRefs } from 'vue';
const props=defineProps({
    headertxt: String,
    
    
})
const state = reactive({
    
    headertxt:props.headertxt,
    

})


const { headertxt } = toRefs(state)
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
        margin-left: 10px;
    }

    .noteheader-headertxt-c {
        width: 160px;
        overflow: hidden;
        margin-right: 16px;
        text-align: left;
        font-size: 15px;

    }

    .noteheader-moretool-c {
        margin-right: 0px;
        display:none;
    }



}
.noteheader-btn-c:hover .noteheader-moretool-c {
    display:block;
}
.noteheader-btn-c:hover .noteheader-headertxt-c {
    width: 120px;
}
</style>