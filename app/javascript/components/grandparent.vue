<template>
    <div>
        <legal-description :legal.sync="legals[0]"></legal-description>
        <legal-description :legal.sync="legals[1]"></legal-description>
    </div>
</template>

<script>
    import legalDescription from './legal-desc'

    export default {
        name: "grandparent",
        components: {
            legalDescription
        },
        data() {
            return {
                legals: [{}, {}]
            }
        }
    }
</script>

<style scoped>

</style>