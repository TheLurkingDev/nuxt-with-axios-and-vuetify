<template>
    <div>
        {{ $route.params.id }}
        {{ albumData }}
    </div>
</template>

<script>
import axios from 'axios';

export default {
    asyncData({ params }) {
        return axios.get(`https://itunes.apple.com/search?term=${params.id}&entity=album`)
        .then((response) => {
            return { albumData: response.data.results }
        });
    },

    middleware: 'search'
}
</script>
