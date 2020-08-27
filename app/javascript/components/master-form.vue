<template>
    <div id="master-form">
        <h3>master-form component</h3>
        mockAxiosData:
        <p style="white-space: pre">{{JSON.stringify(mockAxios, null, 4)}}</p>
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
                    legals: [
                        {state: 'Texas', county: 'Andrews'},
                        {state: 'Oklahoma', county: 'BEAVER'}
                    ],
                    xrefs: [
                        {number: '001', name: 'test.pdf'}
                    ]
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