<template>
    <nav class="navbar">
        <div class="photo">
            <img src="../assets/moi.png" alt="Moi" />
        </div>
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
        <div class="btns">
            <button type="button" @click="emitLangChanged('fr')" :class="lang === 'fr' ? 'active' : ''">FR</button>
            <button type="button" @click="emitLangChanged('en')" :class="lang === 'en' ? 'active' : ''">EN</button>
        </div>
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
            emitLangChanged(lang) {
                this.$emit('langChanged', lang);
            },
        },
    };
</script>

<style scoped lang="scss">

    nav {
        height: 100%;
        background: #54a8c3;

        img {
            display: block;
            margin: 0 auto;
            height: 100px;
            width: auto;
            box-shadow: 1px 1px 5px #777;
            border-radius: 50%;
            object-fit: contain;
            background-color: rgba(238, 238, 238, 0.53);
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
                    background-color: rgb(107, 107, 107);
                }
            }
        }
        .btns {
            position: absolute;
            width: 100%;
            left: 0;
            bottom: 10px;
            text-align: center;
            button {
                border: none;
                box-shadow: none;
                outline: none;
                cursor: pointer;

                &.active {
                    background-color: #777777;
                    color: #fff;
                }
            }
        }
    }
</style>
