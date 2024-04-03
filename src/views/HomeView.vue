<script>
    import AppCarousel from '@/components/AppCarousel.vue'
    import SinglePost from '@/components/SinglePost.vue'

    export default {
        name: "HomeView",
        components: {
            AppCarousel,
            SinglePost
        },
        data() {
            return {
                posts: [
                    {
                        id: 0,
                        img: 'https://picsum.photos/id/237/500/600',
                        description: 'Everything you need',
                        like: 180,
                        author: {
                            id: 0,
                            name: 'thetrueluca',
                            avatar: 'https://picsum.photos/id/217/300/300'
                        }
                    },
                    {
                        id: 1,
                        img: 'https://picsum.photos/id/267/500/600',
                        description: 'Everything you need',
                        like: 110,
                        author: {
                            id: 1,
                            name: 'youssef',
                            avatar: 'https://picsum.photos/id/117/300/300'
                        }
                    },
                    {
                        id: 2,
                        img: 'https://picsum.photos/id/564/500/600',
                        description: 'Everything you need',
                        like: 170,
                        author: {
                            id: 2,
                            name: 'ercole',
                            avatar: 'https://picsum.photos/id/217/300/300'
                        }
                    },
                    {
                        id: 3,
                        img: 'https://picsum.photos/id/231/500/600',
                        description: 'Everything you need',
                        like: 2345,
                        author: {
                            id: 4,
                            name: 'jhonny__',
                            avatar: 'https://picsum.photos/id/756/300/300'
                        }
                    },
                ]
            }
        }
    }
</script>

<template>
    <div class="container">
        <main>
            <div class="for-you">
                <p class="active">Per te</p>
                <p>Seguiti</p>
            </div>
            <AppCarousel />
            <div class="post-wrapper">
                <SinglePost v-for="post in posts" :post="post" />
            </div>
        </main>
    </div>
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;
@use '../assets/scss/partials/mixins' as *;

.container {
    width: 100vw;
    height: 100vh;
    padding-top: 32px;
    color: white;
    overflow-y: scroll;
    @include flex(center);
    
    main {
        max-width: 630px;

        .for-you {
            width: 100%;
            padding: 0.8rem 0;
            border-bottom: 1px solid #262626;
            @include flex(start, center);

            p {
                color: $text-color;
                font-size: 16px;
                margin-right: 1rem;
                font-weight: 600;

                &.active {
                    color: white;
                }
            }
        }

        .post-wrapper {
            width: 100%;
            margin-top: .5rem;
            @include flex(center, center, column);
        }
    }
}

@media screen and (max-width: 768px) {

    .container {
        padding-top: 0;

        main {
            min-width: 100%;

            .for-you {
                display: none !important;
                background-color: red;
            }
        }
    }
}
</style>
