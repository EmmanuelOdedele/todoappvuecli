<template>
  <div class="container">
    <h2 class="text-center mt-5">My Vue Todo App</h2>

    <!-- Input -->
    <div class="d-flex mt-5">
      <input type="text" placeholder="Enter task" class="form-control" />
      <button class="btn btn-warning">SUBMIT</button>
    </div>

    <!--Task-->
    <table class="table table-bordered mt-5">
      <thead>
        <tr>
          <th scope="col">Task</th>
          <th scope="col">Status</th>
          <th scope="col" class="text-center">Edit</th>
          <th scope="col" class="text-center">Delete</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(task, index) in tasks" :key="index">
          <td>{{ task.name }}</td>
          <td>{{ task.status }}</td>
          <td>
            <div class="text-center">
              <span class="fa fa-pen"></span>
            </div>
          </td>
          <td>
            <div class="text-center">
              <span class="fa fa-trash"></span>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },

  data() {
    return {
      tasks: [
        {
          name: "Prayer",
          status: "to-do",
        },
        {
          name: "Bible reading",
          status: "to-do",
        },
        {
          name: "Sleep",
          status: "to-do",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
