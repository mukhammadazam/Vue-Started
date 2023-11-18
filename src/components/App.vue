<template>
  <div class="container">
    <div class="d-flex align-items-center justify-content-center mt-5">
      <button @click="increment" class="btn btn-success d-block me-3">
        Increment
      </button>
      <p class="p-0">
        <strong> {{ count }}</strong>
      </p>
      <button @click="decrement" class="btn btn-primary ms-3">Decrement</button>
    </div>
  <div class="comments" v-for="comment in comments" v-bind:key="comment.index">
<div   class="comment  border mt-5 p-5 border-3">
    <p class="text ps-5"><strong class="strong">Name:</strong>{{ comment.Name }}</p>
    <p class="text ps-5"><strong class="strong">Email:</strong>{{ comment.Email }}</p>
    <p class="text ps-5"><strong class="strong">Content:</strong>{{ comment.Content}}</p>
</div>
</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      comments: [
        {
          Name: "Rizayev Mukhammad A'zam",
          Email: "rizayevmuhammadazam9@gmail.com",
          Content: "Lorem, ipsum dolor.",
        }, {
          Name: "Rizayev Mukhammad A'zam",
          Email: "rizayevmuhammadazam9@gmail.com",
          Content: "Lorem, ipsum dolor.",
        }
        
      ],
    };
  },
  methods: {
    increment() {
      this.count += 1;
    },
    decrement() {
      this.count -= 1;
    },
  },
};
</script>
<style>
.comment {
  width: 600px;
  margin: 0 auto;
  border-radius: 10px;
}
</style>
