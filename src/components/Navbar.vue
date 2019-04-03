<template>
    <nav class="navbar">
        <button type="button" @click="emitLangChanged">Changer langue</button>
        <ul>
            <li>
                <a href="#presentation">
                    Présentation
                </a>
            </li>
            <li>
                <a href="#experiences">
                    Expériences
                </a>
            </li>
            <li>
                <a href="#competences">
                    Compétences
                </a>
            </li>
            <li>
                <a href="#formations">
                    Formations
                </a>
            </li>
        </ul>
    </nav>
</template>

<script>
    export default {
        name: 'Navbar',
        props: {
            lang: {
                type: String,
                default: 'fr',
            },
        },
        methods: {
            emitLangChanged() {
                this.$emit('langChanged');
            },
        },
    };
</script>

<style scoped lang="scss">

    nav {
        height: 100%;
        background: #54a8c3;
    }

    ul {
        position: absolute;
        height: 253px;
        width: 100%;
        top: calc(50% - (253px / 2));

        padding: 0;
        margin: 0;
        list-style: none;


        a {
            display: block;
            height: 100%;
            width: 100%;
            color: #fff;
            font-size: 22px;
            padding: 10px 10px 10px 40px;

            &:hover, &.active {
                background-color: rgb(156, 156, 156);
            }
        }
    }
</style>
