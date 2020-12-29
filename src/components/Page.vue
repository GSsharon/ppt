<!--
 * @Author: sharon
 * @Date: 2020-12-29 17:59:39
 * @LastEditTime: 2020-12-29 18:31:36
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \ppt\src\components\Page.vue
-->
<template>
    <div class="page">
        <h3 v-if="pageTitle">{{pageTitle}}</h3>
        <div class="content">
            <p v-if="typeof content == 'String'">{{content}}</p>
            <ul v-if="typeof content != 'String'">
                <li v-for="(todo, idx) in content" :key="idx">
                    <h4 v-if="todo.title">{{todo.title}}</h4>
                    <div class="description">{{todo.description}}</div>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        pageTitle: {
            type: String,
            default: ''
        }, 
        content: {
            type: [String, Array],
            default: ''
        }
    },
    created() {
        console.log(this.pageTitle)
    },
    data() {
        return {

        }
    }
}
</script>
<style lang="scss" scoped>
    .page {
        height: 100vh;
        h3 {
            text-align: center;
        }
        .content {
            margin: 0 auto;
        }
    }
</style>
