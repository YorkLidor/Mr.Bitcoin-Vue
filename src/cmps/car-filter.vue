<template>
    <div class="car-filter">
        <p>Search</p>
        <input @input="onFilter" v-model="filterBy.txt" type="text">
    </div>
</template>

<script>
export default {
    data() {
        return {
            filterBy: {
                txt: '',
            }
        }
    },
    methods: {
        onFilter() {
            this.$emit('filter', this.filterBy)
        }
    }
}
</script>

<style lang="scss"></style>
