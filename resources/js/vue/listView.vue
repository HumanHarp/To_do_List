<template>
    <div>
        <div v-for="(item, index) in items" :key="index">
            <ListItem
            :item="item"
            class="item"
            v-on:itemchanged="$emit('reloadlist')"
            />
        </div>
    </div>
</template>

<script>
import ListItem from "./ListItem"
export default{
    props: ['items'],
    components:{
        ListItem
    }
}
</script>

<style scoped>

.item{
    background: #e6e6e6;
    padding: 5px;
    margin-top: 5px;
}

</style>