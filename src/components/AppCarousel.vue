<script>
    export default {
        name: "AppCarousel",
        data() {
            return {
                activeIndex: 0,
                stories: [
                    {
                        img: 'https://picsum.photos/id/237/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/232/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/257/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/217/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/277/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/217/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/537/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/137/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/232/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/517/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/133/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/135/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/634/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/432/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/675/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/324/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/162/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/742/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/213/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/163/300/300',
                    },
                    {
                        img: 'https://picsum.photos/id/453/300/300',
                    },
                ],
            }
        },
        methods: {
            next() {
                this.activeIndex++;
            },
            prev() {
                this.activeIndex--;
            }
        }
    }
</script>

<template>
    <div class="carousel">
        <div class="stories" :style="{ transform: `translateX(${-activeIndex * 630}px)` }">
            <div class="story" v-for="story in stories">
                <div class="circle">
                    <img :src="story.img" alt="">
                </div>
            </div>
        </div>
        <button class="prev" :class=" activeIndex == 0 ? 'd-none' : '' " @click="prev()">
            <svg width="15" height="15" viewBox="0 0 1024 1024" fill="#000000" class="icon">
                <path d="M669.6 849.6c8.8 8 22.4 7.2 30.4-1.6s7.2-22.4-1.6-30.4l-309.6-280c-8-7.2-8-17.6 0-24.8l309.6-270.4c8.8-8 9.6-21.6 2.4-30.4-8-8.8-21.6-9.6-30.4-2.4L360.8 480.8c-27.2 24-28 64-0.8 88.8l309.6 280z" fill="" />
            </svg>
        </button>
        <button class="next" :class=" parseInt(stories.length / 8) == activeIndex ? 'd-none' : '' " @click="next()">
            <svg width="15" height="15" viewBox="0 0 1024 1024" fill="#000000" class="icon" style="transform: rotate(180deg);">
                <path d="M669.6 849.6c8.8 8 22.4 7.2 30.4-1.6s7.2-22.4-1.6-30.4l-309.6-280c-8-7.2-8-17.6 0-24.8l309.6-270.4c8.8-8 9.6-21.6 2.4-30.4-8-8.8-21.6-9.6-30.4-2.4L360.8 480.8c-27.2 24-28 64-0.8 88.8l309.6 280z" fill="" />
            </svg>
        </button>
    </div>
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;
@use '../assets/scss/partials/mixins' as *;

.carousel {
    width: 100%;
    padding: 1rem .5rem;
    position: relative;
    overflow: hidden;

    .stories{
        width: 100%;
        display: flex;
        transition: transform 0.5s ease;
    }

    .story {
        width: 70px;
        flex: 0 0 auto;

        .circle {
            width: 55px;
            height: 55px;
            border-radius: 50%;
            overflow: hidden;
            position: relative;
            background-image: linear-gradient(
                    45deg,
                    #ffa95f 5%,
                    #f99c4a 15%,
                    #f47838 30%,
                    #e75157 45%,
                    #d92d7a 70%,
                    #cc2a92 80%,
                    #c32e92 95%
                );
            padding: 3px;
            
            img {
                width: 100%;
                height: 100%;
                border-radius: 50%;
                object-fit: cover;
                object-position: center;
            }
        }
    }

    button {
        width: 20px;
        height: 20px;
        position: absolute;
        border: none;
        border-radius: 50%;
        background-color: white;
        top: 50%;
        transform: translateY(-50%);
        @include flex(center, center);

        &.prev {
            left: 5px;
            padding: 0.1rem 0.25rem 0.2rem 0.1rem;
        }

        &.next {
            right: 5px;
            padding-bottom: 0.02rem;
        }
    }
}
</style>