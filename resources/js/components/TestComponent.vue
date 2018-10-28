<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-6" v-for="value in cards">
                <div class="card card-default">
                    <div class="card-header">Test Component</div>

                    <div class="card-body">
                        This is {{ prefixCard(value) }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            // 一進來要做的事情
            console.log('Component mounted.')
        },
        data() {
            // 定義會用到的資料們
            return {
                cards: ['cardA', 'meow', 'neko', 'gopher']
            }
        },
        methods: {
            // 定義會用到的 function們
            prefixCard(cardName) {
                return `Oo.${cardName}.oO`
            }
        }
    }
</script>
