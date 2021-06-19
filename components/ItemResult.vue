<template>
  <div>
    <div v-for="company in filteredData" :key="company.id">
      <div class="container items m-auto my-16">
        <div class="grid justify-items-end p-4 text-gray">
          {{ company.code }}
        </div>
        <div class="px-12">
          <div class="flex flex-row">
            <img :src="company.logo" alt="" class="" />
            <div class="grid justify-items-start ml-6 class=text-blue">
              <div>{{ company.name }}</div>
              <div>{{ company.location }}</div>
              <div>⭐⭐⭐⭐⭐ <a href=""> 100 reviews</a></div>
            </div>
          </div>
          <div class="px-12 mt-12">
            <p class="content text-blue">{{ company.content }}</p>
          </div>
          <button
            class="text-white font-bold py-2 px-4 border border-blue-700 rounded mt-12"
          >
            Request Quote
          </button>
        </div>
      </div>
    </div>

    <button @click="limit = null" class="show-more">See more</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      limit: 5,
      companies: [
        {
          name: "Company Name #1",
          code: "ABN 62 502 909 410",
          location: "Manchester",
          logo: require("~/assets/svg/company-icon.svg"),
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        },
        {
          name: "Company Name #2",
          code: "ABN 62 502 909 411",
          location: "Manchester",
          logo: require("~/assets/svg/company-icon.svg"),
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        },
        {
          name: "Company Name #3",
          code: "ABN 62 502 909 412",
          location: "Manchester",
          logo: require("~/assets/svg/company-icon.svg"),
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        },
        {
          name: "Company Name #4",
          code: "ABN 62 502 909 413",
          location: "Manchester",
          logo: require("~/assets/svg/company-icon.svg"),
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        },
        {
          name: "Company Name #5",
          code: "ABN 62 502 909 414",
          location: "Manchester",
          logo: require("~/assets/svg/company-icon.svg"),
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        },
        {
          name: "Company Name #6",
          code: "ABN 62 502 909 415",
          location: "Manchester",
          logo: require("~/assets/svg/company-icon.svg"),
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        },
        {
          name: "Company Name #7",
          code: "ABN 62 502 909 416",
          location: "Manchester",
          logo: require("~/assets/svg/company-icon.svg"),
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        }
      ]
    };
  },
  computed: {
    filteredData() {
      return this.limit ? this.companies.slice(0, this.limit) : this.companies;
    }
  }
};
</script>

<style>
.items {
  width: 1016px;
  height: 477px;
  background: #ffffff;
  box-shadow: 0px 35px 50px rgba(0, 0, 0, 0.05);
  border-radius: 20px;
}

button {
  background: #38547b;
}

.content {
  text-align: justify;
  text-justify: inter-word;
}
.show-more {
  border: 1px solid #38547b;
  background: white;
  width: 145px;
  height: 55px;
}
</style>
