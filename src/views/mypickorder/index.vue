<template>
<div>
<!-- table -->
<div class="pad"> 
    <div class="ui top attached button orange" tabindex="0">
        <span style="    padding-right: 26px;">去app接单</span>
        <i class="plus icon"></i>
    </div>
    <div class="tableflex">
        <table class="ui celled padded table">
        <thead>
            <tr><th class="single line">订单状态</th>
            <th>订单金额</th>
            <th>订单类型</th>
            <th>订单地址</th>
            <th>订单时间</th>
            <th>订单内容</th>
            <th>操作</th>
        </tr></thead>
        <tbody v-if="islogin">
            <tr>
            <td>
                <h2 class="ui center aligned header">已接单</h2>
            </td>
            <td class="single line center" >3元 </td>
            <td>
                帮拿快递 
            </td>
            <td>六号楼一单元</td>
            <td class=" aligned">提交:2022-9-30 09:04:26<br> 过期: 2022-10-3 09:04:26</td>
            <td>快递是小件 取件码为B-1-2</td>
            <td><button class="ui grey basic button">放弃订单</button><br>
            </td>
            </tr>
            <tr>
            <td>
                <h2 class="ui center aligned header">已接单</h2>
            </td>
            <td class="single line center">3元 </td>
            <td>
                帮拿快递 
            </td>
            <td>六号楼一单元</td>
            <td class=" aligned">提交:2022-9-30 09:04:26<br> 过期: 2022-10-3 09:04:26</td>
            <td>快递是小件 取件码为B-1-2</td>
            <td><button class="ui grey basic button">放弃订单</button><br>
            </td>
            </tr>
            <tr>
            <td>
                <h2 class="ui center aligned header">已接单</h2>
            </td>
            <td class="single line center">3元 </td>
            <td>
                帮拿快递 
            </td>
            <td>六号楼一单元</td>
            <td class=" aligned">提交:2022-9-30 09:04:26<br> 过期: 2022-10-3 09:04:26</td>
            <td>快递是小件 取件码为B-1-2</td>
            <td><button class="ui grey basic button">放弃订单</button><br>
            </td>
            </tr>
            <tr>
            <td>
                <h2 class="ui center aligned header">已接单</h2>
            </td>
            <td class="single line center">3元 </td>
            <td>
                帮拿快递 
            </td>
            <td>六号楼一单元</td>
            <td class=" aligned">提交:2022-9-30 09:04:26<br> 过期: 2022-10-3 09:04:26</td>
            <td>快递是小件 取件码为B-1-2</td>
            <td><button class="ui grey basic button">放弃订单</button><br>
            </td>
            </tr>
            <tr>
            <td>
                <h2 class="ui center aligned header">已接单</h2>
            </td>
            <td class="single line center">3元 </td>
            <td>
                帮拿快递 
            </td>
            <td>六号楼一单元</td>
            <td class=" aligned">提交:2022-9-30 09:04:26<br> 过期: 2022-10-3 09:04:26</td>
            <td>快递是小件 取件码为B-1-2</td>
            <td><button class="ui grey basic button">放弃订单</button><br>
            </td>
            </tr>

        </tbody>
        </table>
    </div>

</div>
<!-- 数据为空的时候显示 -->
<el-empty description="暂无接单信息！" v-if="!mypickorderList"></el-empty>
<el-empty description="请先登录！" v-if="!islogin"></el-empty>
<!-- 分页组件 -->
<!-- <div class="page">
    <el-pagination
    page-size="5"
    background="true"
    layout="prev, pager, next"
    :total="10">
    </el-pagination>
</div> -->
</div>

</template>

<script>
export default {
    data(){
    return {
        //订单列表
        mypickorderList:[1],
    }
},
//判断是否登录
computed:{
    islogin(){
        return this.$store.state.islogin
    }
}
}
</script>

<style lang="less" scoped>
.pad{
    padding-top: 30px;
}
.ui.celled.padded.table{
    width: 1200px;
}

.ui.top.attached.button{
    width: 1200px;
    height: 70px;
    margin: auto;
    display: flex;
    flex-direction: column;
    align-items: center;


}
.tableflex{
    display: flex;
    justify-content: center;
}
.ui.grey.basic.button{
    margin-top: 2px;
    font-size: 10px;
}
.plus.icon{
    font-size: 40px;
    padding-top: 15px;
}
.page{
    padding-top: 20px;
    display: flex;
    justify-content: center;
}
</style>