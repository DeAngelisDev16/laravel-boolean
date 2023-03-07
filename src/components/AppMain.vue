<script>
import axios from 'axios';
export default {
    name: 'AppMain',
    //components
    data() {
        return {

            booksList: [],
            apiUrl: 'http://127.0.0.1:8000/api/books',

        }
    },
    methods: {
        getBooks() {
            const self = this;

            axios.get(this.apiUrl, {
                params: {

                }
            })
                .then(function (response) {
                    console.log(response.data.results);
                    self.booksList = response.data.results;


                })
                .catch(function (error) {
                    console.log(error);
                })
                .then(function () {
                    // always executed
                });
        },




    },
    created() {
        this.getBooks()

    }

}

</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-3" v-for="book in booksList">
                <div class="card">
                    <h3>{{ book.title }}</h3>
                    <h4>{{ book.author }}</h4>

                </div>

            </div>
        </div>
    </div>
</template>

<style scoped></style>
