<template>
  <div class="search m-auto flex flex-col">
    <div class="font-bold text-4xl text-blue mt-12">
      Where do you need the job done?
    </div>
    <div class="flex flex-row my-12">
      <input type="text" class="rounded-full input ml-24" />
      <a href=""
        ><img class="ml-12" src="~assets/svg/search-icon.svg" alt=""
      /></a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.input {
  width: 443px;
  height: 65px;
}

input[type="text"] {
  font-size: 18px;
  color: #38547b;
  padding-left: 20px;
}

.search {
  background-color: #deedff;
  width: 749px;
  height: 269px;
  border-radius: 50px;
}
</style>
