<script>
import { store } from '../store/index';

export default {
    data() {
        return {
            genders: [
                {
                    gender: 'Donna',
                },
                {
                    gender: 'Uomo',
                },
                {
                    gender: 'Bambini',
                }

            ],
            icons: [
                {
                    iconName: 'fa-regular fa-user'
                },
                {
                    iconName: 'fa-regular fa-heart'
                },
                {
                    iconName: 'fa-solid fa-cart-shopping'
                }
            ],
            store,
        };
    }
};
</script>
<template>
    <header class="header">
        <div class="container">
            <div class="header-nav-left">
                <ul>
                    <li v-for="sex in genders"><a href="#">{{ sex.gender }}</a></li>

                </ul>
            </div>
            <div class="header-logo-center">

                <img class="logo" src="../assets/img/boolean-logo.png" alt="" />
            </div>
            <div class="header-nav-right">
                <ul>
                    <li v-for="icone in icons">
                        <a href="#" :class="icone.iconName"></a>

                    </li>

                </ul>
            </div>
        </div>
    </header>
</template>
<style lang="scss"></style>