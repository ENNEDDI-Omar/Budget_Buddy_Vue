<template>
  <div class="bg-white dark:bg-gray-900">
    <div class="flex justify-center h-screen">
      <div class="flex items-center w-full max-w-md px-6 mx-auto lg:w-2/6">
        <div class="flex-1">
          <div class="text-center">
            <div class="flex justify-center mx-auto">
              <img
                class="w-auto h-7 sm:h-8"
                src="https://merakiui.com/images/logo.svg"
                alt=""
              />
            </div>
            <p class="mt-3 text-gray-500 dark:text-gray-300">
              Create an account to get started
            </p>
          </div>
          <div class="mt-8">
            <form @submit.prevent="register">
              <div>
                <label
                  for="name"
                  class="block mb-2 text-sm text-gray-600 dark:text-gray-200"
                  >Full Name</label
                >
                <input
                  type="text"
                  v-model="user.name"
                  id="name"
                  placeholder="Your Full Name"
                  class="block w-full px-4 py-2 mt-2 text-gray-700 placeholder-gray-400 bg-white border border-gray-200 rounded-lg dark:placeholder-gray-600 dark:bg-gray-900 dark:text-gray-300 dark:border-gray-700 focus:border-blue-400 dark:focus:border-blue-400 focus:ring-blue-400 focus:outline-none focus:ring focus:ring-opacity-40"
                />
              </div>
              <div class="mt-6">
                <label
                  for="email"
                  class="block mb-2 text-sm text-gray-600 dark:text-gray-200"
                  >Email Address</label
                >
                <input
                  type="email"
                  v-model="user.email"
                  id="email"
                  placeholder="example@example.com"
                  class="block w-full px-4 py-2 mt-2 text-gray-700 placeholder-gray-400 bg-white border border-gray-200 rounded-lg dark:placeholder-gray-600 dark:bg-gray-900 dark:text-gray-300 dark:border-gray-700 focus:border-blue-400 dark:focus:border-blue-400 focus:ring-blue-400 focus:outline-none focus:ring focus:ring-opacity-40"
                />
              </div>
              <div class="mt-6">
                <label
                  for="password"
                  class="block mb-2 text-sm text-gray-600 dark:text-gray-200"
                  >Password</label
                >
                <input
                  type="password"
                  v-model="user.password"
                  id="password"
                  placeholder="Your Password"
                  class="block w-full px-4 py-2 mt-2 text-gray-700 placeholder-gray-400 bg-white border border-gray-200 rounded-lg dark:placeholder-gray-600 dark:bg-gray-900 dark:text-gray-300 dark:border-gray-700 focus:border-blue-400 dark:focus:border-blue-400 focus:ring-blue-400 focus:outline-none focus:ring focus:ring-opacity-40"
                />
              </div>
              <div class="mt-6">
                <button
                  type="submit"
                  class="w-full px-4 py-2 tracking-wide text-white transition-colors duration-300 transform bg-blue-500 rounded-lg hover:bg-blue-400 focus:outline-none focus:bg-blue-400 focus:ring focus:ring-blue-300 focus:ring-opacity-50"
                >
                  Sign Up
                </button>
              </div>
            </form>
            <p class="mt-6 text-sm text-center text-gray-400">
              Already have an account?
              <a
                href="#"
                class="text-blue-500 focus:outline-none focus:underline hover:underline"
                >Sign in</a
              >.
            </p>
          </div>
        </div>
      </div>
      <div
        class="hidden bg-cover lg:block lg:w-2/3"
        style="
          background-image: url(https://images.unsplash.com/photo-1616763355603-9755a640a287?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80);
        "
      >
        <div class="flex items-center h-full px-20 bg-gray-900 bg-opacity-40">
          <div>
            <h2 class="text-2xl font-bold text-white sm:text-3xl">
              Budget Buddy
            </h2>
            <p class="max-w-xl mt-3 text-gray-300">
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. In autem
              ipsa, nulla laboriosam dolores, repellendus perferendis libero
              suscipit nam temporibus molestiae
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      user: {
        name: "",
        email: "",
        password: "",
      },
    };
  },

  methods: {
    register() {
      axios
        .post("http://localhost:8000/api/register", this.user)
        .then((response) => {
          // Handle the API response here
          console.log("API response:", response.data);
          alert(response.data.message);
        })
        .catch((error) => {
          // Handle errors here
          if (error.response) {
            // The request was made and the server responded with a status code
            // that falls out of the range of 2xx
            console.error("Error:", error.response.data);
          } else if (error.request) {
            // The request was made but no response was received
            console.error("Error: No response was received", error.request);
          } else {
            // Something happened in setting up the request that triggered an Error
            console.error("Error", error.message);
          }
          alert("Error during the request: " + error.message);
        });
    },
  },
};
</script>
