<template>
  <div class="">
    <div class="text-center my-20">
      <div class="container cards m-auto">
        <SearchForm />
      </div>
      <div>
        <p class="font-bold text-blue mt-14 f-35">
          Local Businessess Near You
        </p>
        <p class="font-bold mt-8 mb-4 filterby">Filter by</p>
        <button class="mx-8 filters" @click="changeColor">Ratings</button>
        <button href="" class="mx-8 filters" @click="changeColor">
          Review
        </button>
        <button class="mx-8 filters" @click="changeColor">Name</button>
        <button class="mx-8 filters mb-16" @click="changeColor">Nearest</button>
        <ItemResult />
      </div>
    </div>
  </div>
</template>

<script>
import SearchForm from "~/components/SearchForm.vue";
import ItemResult from "~/components/ItemResult.vue";
export default {
  components: {
    SearchForm,
    ItemResult
  }
};
</script>

<style>
body {
  background: #fcfcfc;
}
.filters {
  background-color: #fcfcfc;
}

.filters:focus {
  text-decoration: underline;
  outline: none;
}
.text-blue,
.filters:focus {
  color: #38547b;
}
.text-gray,
.filters {
  color: #d6d6d6;
}

.f-35 {
  font-size: 35px;
}

.filterby {
  color: #717171;
}
</style>
