<script>
    export default {
        name: "MobileHeader"
    }
</script>

<template>
    <header>
        <div class="upper-header">
            <div class="container">
                <div class="for-you">
                    Per te
                    <svg width="12" height="12" fill="#ffffff" viewBox="0 0 24 24" ><title>Freccia verso il basso</title>
                        <path d="M12 17.502a1 1 0 0 1-.707-.293l-9-9.004a1 1 0 0 1 1.414-1.414L12 15.087l8.293-8.296a1 1 0 0 1 1.414 1.414l-9 9.004a1 1 0 0 1-.707.293Z"></path>
                    </svg>
                </div>
                <div class="search">
                    <div class="input-control">
                        <div>
                            <svg width="16" height="16" fill="#ffffff" viewBox="0 0 24 24" ><title>Cerca</title>
                                <path d="M19 10.5A8.5 8.5 0 1 1 10.5 2a8.5 8.5 0 0 1 8.5 8.5Z" fill="none" stroke="#818181" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
                                <line fill="none" stroke="#818181" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="16.511" x2="22" y1="16.511" y2="22"></line>
                            </svg>
                        </div>
                        <input type="text" placeholder="Cerca">
                    </div>
                    <div class="heart">
                        <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Notifiche</title>
                            <path d="M16.792 3.904A4.989 4.989 0 0 1 21.5 9.122c0 3.072-2.652 4.959-5.197 7.222-2.512 2.243-3.865 3.469-4.303 3.752-.477-.309-2.143-1.823-4.303-3.752C5.141 14.072 2.5 12.167 2.5 9.122a4.989 4.989 0 0 1 4.708-5.218 4.21 4.21 0 0 1 3.675 1.941c.84 1.175.98 1.763 1.12 1.763s.278-.588 1.11-1.766a4.17 4.17 0 0 1 3.679-1.938m0-2a6.04 6.04 0 0 0-4.797 2.127 6.052 6.052 0 0 0-4.787-2.127A6.985 6.985 0 0 0 .5 9.122c0 3.61 2.55 5.827 5.015 7.97.283.246.569.494.853.747l1.027.918a44.998 44.998 0 0 0 3.518 3.018 2 2 0 0 0 2.174 0 45.263 45.263 0 0 0 3.626-3.115l.922-.824c.293-.26.59-.519.885-.774 2.334-2.025 4.98-4.32 4.98-7.94a6.985 6.985 0 0 0-6.708-7.218Z"></path>
                        </svg>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Bottom Header -->
    <div class="bottom-header">
        <div class="container">
            <div class="icon-wrapper">
                <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Home</title>
                    <path d="M22 23h-6.001a1 1 0 0 1-1-1v-5.455a2.997 2.997 0 1 0-5.993 0V22a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1V11.543a1.002 1.002 0 0 1 .31-.724l10-9.543a1.001 1.001 0 0 1 1.38 0l10 9.543a1.002 1.002 0 0 1 .31.724V22a1 1 0 0 1-1 1Z"/>
                </svg>
            </div>
            <div class="icon-wrapper">
                <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Esplora</title>
                    <polygon fill="none" points="13.941 13.953 7.581 16.424 10.06 10.056 16.42 7.585 13.941 13.953" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
                    <polygon fill-rule="evenodd" points="10.06 10.056 13.949 13.945 7.581 16.424 10.06 10.056"/>
                    <circle cx="12.001" cy="12.005" fill="none" r="10.5" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
                </svg>
            </div>
            <div class="icon-wrapper">
                <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Reels</title>
                    <line fill="none" stroke="#ffffff" stroke-linejoin="round" stroke-width="2" x1="2.049" x2="21.95" y1="7.002" y2="7.002"/>
                    <line fill="none" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="13.504" x2="16.362" y1="2.001" y2="7.002"/>
                    <line fill="none" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="7.207" x2="10.002" y1="2.11" y2="7.002"/>
                    <path d="M2 12.001v3.449c0 2.849.698 4.006 1.606 4.945.94.908 2.098 1.607 4.946 1.607h6.896c2.848 0 4.006-.699 4.946-1.607.908-.939 1.606-2.096 1.606-4.945V8.552c0-2.848-.698-4.006-1.606-4.945C19.454 2.699 18.296 2 15.448 2H8.552c-2.848 0-4.006.699-4.946 1.607C2.698 4.546 2 5.704 2 8.552Z" fill="none" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
                    <path d="M9.763 17.664a.908.908 0 0 1-.454-.787V11.63a.909.909 0 0 1 1.364-.788l4.545 2.624a.909.909 0 0 1 0 1.575l-4.545 2.624a.91.91 0 0 1-.91 0Z" fill-rule="evenodd"/>
                </svg>
            </div>
            <div class="icon-wrapper">
                <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Nuovo post</title>
                    <path d="M2 12v3.45c0 2.849.698 4.005 1.606 4.944.94.909 2.098 1.608 4.946 1.608h6.896c2.848 0 4.006-.7 4.946-1.608C21.302 19.455 22 18.3 22 15.45V8.552c0-2.849-.698-4.006-1.606-4.945C19.454 2.7 18.296 2 15.448 2H8.552c-2.848 0-4.006.699-4.946 1.607C2.698 4.547 2 5.703 2 8.552Z" fill="none" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
                    <line fill="none" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="6.545" x2="17.455" y1="12.001" y2="12.001"/>
                    <line fill="none" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="12.003" x2="12.003" y1="6.545" y2="17.455"/>
                </svg>
            </div>
            <div class="icon-wrapper">
                <svg width="24" height="24" fill="#ffffff" viewBox="0 0 24 24"><title>Direct</title>
                    <line fill="none" stroke="#ffffff" stroke-linejoin="round" stroke-width="2" x1="22" x2="9.218" y1="3" y2="10.083"/>
                    <polygon fill="none" points="11.698 20.334 22 3.001 2 3.001 9.218 10.084 11.698 20.334" stroke="#ffffff" stroke-linejoin="round" stroke-width="2"/>
                </svg>
            </div>
            <div class="icon-wrapper">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none"><title>Profilo</title>
                    <path d="M16 7C16 9.20914 14.2091 11 12 11C9.79086 11 8 9.20914 8 7C8 4.79086 9.79086 3 12 3C14.2091 3 16 4.79086 16 7Z" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    <path d="M12 14C8.13401 14 5 17.134 5 21H19C19 17.134 15.866 14 12 14Z" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;
@use '../assets/scss/partials/mixins' as *;

header {
    width: 100vw;
    height: 60px;
    padding: 0 16px;
    display: none;
    color: white;
    border-bottom: 1px solid #262626;
    
    .upper-header {
        position: sticky;
        height: 100%;

        .container {
            height: 100%;
            @include flex(space-between, center);

            .for-you {
                font-size: 23px;
                font-weight: bold;
            }

            .search {
                width: 60%;
                @include flex(center, center);

                .input-control {
                    width: 80%;
                    @include flex();
                    margin-right: 1rem;

                    div {
                        padding: .6rem .4rem .5rem 0.8rem;
                        border-radius: 10px 0 0 10px;
                        background-color: #262626;
                    }

                    input {
                        width: 100%;
                        border: none;
                        border-radius: 0 10px 10px 0;
                        background-color: #262626;
                    }
                }

                .heart {
                    margin-top: 0.3rem;
                }
            }
        }
    }
}

.bottom-header {
    width: 100%;
    height: 50px;
    display: none;
    position: absolute;
    bottom: 0;
    background-color: black;
    border-top: 1px solid #262626;

    .container {
        width: 100%;
        height: 100%;
        @include flex(space-evenly, center);
    }
}

@media screen and (max-width: 768px) {
    header {
        display: block !important;
    }

    .bottom-header {
        display: block !important;
    }
}
</style>