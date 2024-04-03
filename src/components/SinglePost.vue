<script>
    export default {
        name: "SinglePost",
        props: {
            post: Object
        },
        methods: {
            randomNumber(min, max) {
                return parseInt(Math.random() * (max - min) + min);
            }
        }
    }
</script>

<template>
    <div class="post">
        <header>
            <div class="avatar">
                <img :src="post.author.avatar">
            </div>
            <p>{{ post.author.name }}</p>
            <div class="dot">
                <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Altre opzioni</title>
                    <circle cx="12" cy="12" r="1.5"/>
                    <circle cx="6" cy="12" r="1.5"/>
                    <circle cx="18" cy="12" r="1.5"/>
                </svg>
            </div>
        </header>
        <div class="image">
            <img :src="post.img">
        </div>
        <div class="button-wrapper">
            <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Notifiche</title>
                <path d="M16.792 3.904A4.989 4.989 0 0 1 21.5 9.122c0 3.072-2.652 4.959-5.197 7.222-2.512 2.243-3.865 3.469-4.303 3.752-.477-.309-2.143-1.823-4.303-3.752C5.141 14.072 2.5 12.167 2.5 9.122a4.989 4.989 0 0 1 4.708-5.218 4.21 4.21 0 0 1 3.675 1.941c.84 1.175.98 1.763 1.12 1.763s.278-.588 1.11-1.766a4.17 4.17 0 0 1 3.679-1.938m0-2a6.04 6.04 0 0 0-4.797 2.127 6.052 6.052 0 0 0-4.787-2.127A6.985 6.985 0 0 0 .5 9.122c0 3.61 2.55 5.827 5.015 7.97.283.246.569.494.853.747l1.027.918a44.998 44.998 0 0 0 3.518 3.018 2 2 0 0 0 2.174 0 45.263 45.263 0 0 0 3.626-3.115l.922-.824c.293-.26.59-.519.885-.774 2.334-2.025 4.98-4.32 4.98-7.94a6.985 6.985 0 0 0-6.708-7.218Z"/>
            </svg>
            <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Commenta</title>
                <path d="M20.656 17.008a9.993 9.993 0 1 0-3.59 3.615L22 22Z" fill="none" stroke="#ffffff" stroke-linejoin="round" stroke-width="2"></path>
            </svg>
            <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Direct</title>
                <line fill="none" stroke="#ffffff" stroke-linejoin="round" stroke-width="2" x1="22" x2="9.218" y1="3" y2="10.083"/>
                <polygon fill="none" points="11.698 20.334 22 3.001 2 3.001 9.218 10.084 11.698 20.334" stroke="#ffffff" stroke-linejoin="round" stroke-width="2"/>
            </svg>
            <svg class="save-icon" width="24" height="24" fill="#ffffff" viewBox="0 0 24 24" ><title>Salva</title>
                <polygon fill="none" points="20 21 12 13.44 4 21 4 3 20 3 20 21" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></polygon>
            </svg>
        </div>
        <div class="likes">
            Piace a {{ post.like }} persone
        </div>
        <div class="description">
            <span>{{ post.author.name }}</span> {{ post.description }}
        </div>
        <div class="comments">
            <div>
                Mostra tutti e {{ randomNumber(10, 50) }} i commenti
            </div>
            <input type="text" placeholder="Aggiungi un commento...">
        </div>
    </div>
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;
@use '../assets/scss/partials/mixins' as *;

.post {
    width: 470px;
    padding-bottom: .75rem;
    margin-bottom: .85rem;
    border-bottom: 1px solid #262626;

    header {
        @include flex(start, center);

        .avatar {
            width: 40px;
            height: 40px;
            margin-right: 0.5rem;
            border-radius: 50%;
            overflow: hidden;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: center;
            }
        }

        p {
            padding-bottom: 5px;
            font-size: 15px;
            font-weight: 600;
        }

        .dot {
            height: 100%;
            @include flex(center, center);
            margin-left: auto;
        }
    }

    .image {
        width: 100%;
        height: 600px;
        margin: .75rem 0;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center;
            border-radius: 5px;
        }
    }

    .button-wrapper {
        @include flex();

        & > * {
            margin-right: 1rem;
        }

        .save-icon {
            margin-right: 0;
            margin-left: auto;
        }
    }

    .likes {
        padding: .75rem 0;
        font-size: 14px;
    }

    .description {
        padding-bottom: .75rem;
        font-size: 14px;
        
        span {
            font-weight: 600;
        }
    }
    
    .comments {
        font-size: 14px;
        color: $text-color;
        
        div {
            padding-bottom: .75rem;
        }

        input {
            background-color: transparent;
            border: none;
            color: white;

            &:focus-visible {
                outline: none;
            }

            &::placeholder {
                font-size: 14px;
            }
        }
    }
}

@media screen and (max-width: 768px) {
    .post {
        width: 100%;
    }
}
</style>