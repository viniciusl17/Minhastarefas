<template>
    <div id="tarefa">
        <ul>
            <li v-for="task in lista" :key="task.key">
                <span>{{task.text}}</span>
                <button @click="deletarTarefa(task.key)">Concluir</button>
            </li>            
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Tarefa',
    props:[
        'lista',
        'delete',
    ],
    methods:{
        deletarTarefa(key){
            this.delete(key);
        }
    }   
}
</script>

<style scoped>
    #tarefa{
        white-space: pre-wrap;
        word-wrap: break-word;
    }

    ul{
        list-style: none;
        padding: 0;
        margin-top: 20px;
    }

    ul li{
        padding: 15px 0;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }

    li:not(:first-child){
        border-top: 1px solid #eee;
    }

    span{
        color: #0d2636;
    }

    button{
        cursor: pointer;
        background: #e37781;
        color: #fff;
        border: 0;
        padding: 8px 7px;
        outline: none;
        border-radius: 4px;
    }

</style>