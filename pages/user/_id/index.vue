<template>
    <div>这个页面的参数是：{{$route.params.id}}</div>
</template>

<script>
export default {
    validate (data){

        return /^\d+$/.test(data.params.id)

    }
}
</script>

