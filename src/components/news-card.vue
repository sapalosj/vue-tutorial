<template>
    <div class="row">
        <div class="card my-3">
            <div class="card-header">
                {{  feed.title }}
            </div>
            <div class="card-body">
                <p class="card-text">{{  feed.content }}</p>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import IFeed from './../types/IFeed';
export default defineComponent({
    name:"news-card",
    components:{},
    props: {
        feed: {
            type: Object as PropType<IFeed>,
            // eslint-disable-next-line vue/require-valid-default-prop
            default: {
                content: 'asdasd',
                title: 'asdasd'
            },
        }
    },
    setup () {
        

        return {}
    }
})
</script>

<style scoped>

</style>