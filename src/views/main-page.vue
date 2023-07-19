<template>
    <div class="container mt-5">
        <div class="container">
            <input class="mx-1" type="text" v-model="inputTitle">
            <input class="mx-1" type="text" v-model="inputContent">

            <button @click="addCard">Add</button>
        </div>
        
        <div v-for="(newsFeed,index) in feeds" :key="index">
          <news-card :feed="newsFeed"></news-card>
        </div>
        <!-- <news-card v-if="showCard"></news-card>
        <button @click="toggleShow">Show</button>
        <button @click="toggleHide">Hide</button> -->
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { ref } from 'vue';
import NewsCard from './../components/news-card.vue';
import IFeed from './../types/IFeed';

export default defineComponent({
    name:"main-page",
    components:{
        NewsCard
    },
    setup () {
        const showCard = ref<boolean>(true);

        const inputContent = ref<string>('');
        const inputTitle = ref<string>('');

        const feeds = ref<IFeed[]>([]);

        const title = 'GYM';
        const content = 'WE GO GYM';

        const toggleShow = () : void =>  {
            showCard.value = true;
        }

        const toggleHide = () : void =>  {
            showCard.value = false;
        }


        const addCard = () => {
            feeds.value.push({
                title: inputTitle.value,
                content: inputContent.value
            })
        }

        return {title,content, showCard, feeds,inputContent,inputTitle,toggleShow,toggleHide, addCard}
    }
})
</script>

<style scoped>

</style>