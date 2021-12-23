<template>
    <div class="tina">
        <el-row>
            <el-col :span="7" :offset="4">
                <a href="http://tinaroot.cn" target="_blank">
                    <el-card class="box-card">
                        <div slot="header" class="clearfix">
                            <span>圣诞节快乐</span>

                            <el-button style="float: right; padding: 3px 0" type="text">
                                跳转
                            </el-button>
                        </div>
                        <div class="text item">
                            <img src="http://tinaroot.cn/static/picture/logo.png"/>
                        </div>
                    </el-card>
                </a>
            </el-col>
            <el-col :span="8" :offset="4">
                <a href="http://lottery.tinaroot.cn" target="_blank">
                    <el-card class="box-card">
                        <div slot="header" class="clearfix">
                            <span>Tina九宫格抽奖</span>
                            <el-button style="float: right; padding: 3px 0" type="text">
                                跳转
                            </el-button>
                        </div>
                        <div class="text item">
                            <img src="https://ae04.alicdn.com/kf/H73f2326157ad4e9fbc8c7de7d432830cb.png"/>
                        </div>
                    </el-card>
                </a>
            </el-col>
        </el-row>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    name: 'Tina',
    created() {
        this.f()
    },
    methods: {
        f() {
            axios.get("http://tinaroot.cn/home")
                .then(response => {
                    console.log(response)
                }, err => {
                    console.log(err)
                })
        }
    }
}
</script>


<style scoped>
.tina a {
    text-decoration: none
}

.text {
    font-size: 14px;
}

.item {
    margin-bottom: 18px;
}

.clearfix:before,
.clearfix:after {
    display: table;
    content: "";
}

.clearfix:after {
    clear: both
}

.box-card {
    width: 480px;
}
</style>
