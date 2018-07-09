<template>
    <div>
        <Registration-form></Registration-form>
        <News></News>
    </div>
</template>

<script>
    import News from './News'
    import RegistrationForm from './RegistrationForm'

    export default {
        name: "federation-page",
        components: {
            News,
            RegistrationForm
        }
    }
</script>

<style scoped>

</style>