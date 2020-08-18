<template>
    <div id="county">
        <h1>county component</h1>
        state: {{state}}<br>
        county: <input :value="county"
                      @input="$emit('update:county', $event.target.value)"  />
    </div>
</template>

<script>
    export default {
        name: "county",
        props: ['county', 'state'],
    }
</script>

<style scoped>
    #county {
        background-color: lightgreen;
        width: 300px;
        margin: 10px;
        padding: 10px;
    }
</style>