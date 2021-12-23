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
                            <img src="https://ae02.alicdn.com/kf/Ha19e38d658834a19ba29a90851517849q.png"/>
                        </div>
                    </el-card>
                </a>
            </el-col>
            <el-col :span="8" :offset="4">
                <a href="http://lottery.tinaroot.cn" target="_blank">
                    <el-card class="box-card">
                        <div slot="header" class="clearfix">
                            <span>九宫格抽奖</span>
                            <el-button style="float: right; padding: 3px 0" type="text">
                                跳转
                            </el-button>
                        </div>
                        <div class="text item">
                            <img src="https://ae01.alicdn.com/kf/H8b39c76b0a05462aac2eec7760a4e91c7.png"/>
                        </div>
                    </el-card>
                </a>
            </el-col>
        </el-row>
        <p></p>
        <el-row>
            <el-col :span="8" :offset="4">
                <a href="http://admin.tinaroot.cn" target="_blank">
                    <el-card class="box-card">
                        <div slot="header" class="clearfix">
                            <span>后台管理系统</span>
                            <el-button style="float: right; padding: 3px 0" type="text">
                                跳转
                            </el-button>
                        </div>
                        <div class="text item">
                            <img src="https://ae01.alicdn.com/kf/H8b39c76b0a05462aac2eec7760a4e91c7.png"/>
                        </div>
                    </el-card>
                </a>
            </el-col>

            <el-col :span="8" :offset="3">
                <a href="http://disk.tinaroot.cn" target="_blank">
                    <el-card class="box-card">
                        <div slot="header" class="clearfix">
                            <span>网盘</span>
                            <el-button style="float: right; padding: 3px 0" type="text">
                                跳转
                            </el-button>
                        </div>
                        <div class="text item">
                            <img src="https://ae01.alicdn.com/kf/H8b39c76b0a05462aac2eec7760a4e91c7.png"/>
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
