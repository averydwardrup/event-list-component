<template>
    <div class="container">
        <div class="d-flex g-5">
            <div 
                class="card p-0 col-md-4"
                v-for="{ id, title, excerpt } in events"
                :key="id"
            >
                <img src="https://cdn.pixabay.com/photo/2023/04/25/15/08/church-7950418_960_720.jpg" class="card-img-top" :alt="title">
                <div class="card-body">
                    <h3 class="mt-3">{{ title }}</h3>
                    <div v-html="excerpt" class="card-text"></div>
                </div>
            </div>
        </div>  
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: "EventsList",
    data() {
        return {
            events: undefined,
        }
    },
    mounted() {
        this.fetchEvents()
    },
    methods: {
        async fetchEvents() {
            try {
                const res = await axios.get('YOUR_URL/tribe/events/v1/events')
                this.events = res.data.events
            } catch (error ) {
                console.log(error)
            }
        }
    }
}
</script>