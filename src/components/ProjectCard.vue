<script>

export default {
    props: { project: Object },
    computed: {
        abstract() {
            const content = this.project.content;
            return content.length > 50 ? content.substr(0, 50) + '...' : content;
        }
    }

}

</script>

<template>
    <div class="col">
        <div class="card h-100">
            <img :src="project.image ? project.image : 'https://www.salumianticacortepallavicina.it/wp-content/uploads/2019/10/no-image.jpg'"
                class="card-img-top">
            <div class="card-body">
                <h5 class="card-title">{{ project.title }}</h5>
                <p class="card-text">{{ abstract }}</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use './src/scss/general.scss' as *;
</style>
