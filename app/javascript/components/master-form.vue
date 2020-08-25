<template>
    <div id="master-form">
        <h3>master-form component</h3>
        mockAxiosData:
        {{mockAxios}}
        <property-desc :legals.sync="mockAxios.legals"></property-desc>
    </div>
</template>

<script>
    import propertyDesc from "./property-desc"

    export default {
        name: "master-form",
        components: {
            propertyDesc
        },
        data() {
            return {
                mockAxios: {
                    legals: [{state: 'Texas', county: 'Andrews'}],
                    crossReference: {number: '001', name: ''}
                }
            }
        }
    }
</script>

<style scoped>
    #master-form {
        margin: 20px;
        padding: 20px;
        background-color: lightcoral;
        display: inline-flex;
        flex-direction: column;
    }
</style>