<template>
    <div>
        {{ $route.params.id }}
        {{ $store.state.albums }}
    </div>
</template>

<script>
export default {
    middleware: 'search'
}
</script>
