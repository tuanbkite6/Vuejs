<template>
  <div id="app">
    <p>Click A {{ a }} times</p>
    <p>Click B {{ b }} times</p>
    <button v-on:mouseover="clickA()">Click A</button>
    <button v-on:click="clickB()">ClickB</button>
    <th>
      <tr>
        Name
      </tr>
      <tr>
        <input type="text" id="Name" v-model="name" />
      </tr>
    </th>
    <th>
      <tr>
        age
      </tr>
      <tr>
        <input type="text" id="age" v-model="c" />
      </tr>
    </th>
    <th>
      <tr>
        Job
      </tr>
      <tr>
        <input type="text" id="Job" v-model="job" />
      </tr>
    </th>
    <th>
      <tr>
        Gender
      </tr>
      <tr>
        <select v-model="gender" name="gender" id="">
          <option value="1" selected disabled>
            -----Select your gender-------
          </option>
          <option value="2">Male</option>
          <option value="3">Female</option>
          <option value="4">Other</option>
        </select>
        <button type="submit" @click = "submitForm">Submit</button>
      </tr>
    </th>
  </div>
  <InformationList :users="users"/>
  <h1 v-if="gender == null">Welcome to testing</h1>
  <h1 v-else-if="gender == 2">You is perfect man</h1>
  <h1 v-if="gender == 3">Are you really woman?</h1>
  <h1 v-if="gender == 4">You can join LGPT community</h1>
</template>

<script>
import InformationList from "./InformationList.vue";

export default {
  name: "HelloWorld",
  data() {
    return {
      a: 0,
      b: 0,
      c: null,
      name: "",
      job: "",
      gender: null,
      users: [],
    };
  },
  component: {
    InformationList,
  },
  

  methods: {
    clickA: function () {
      console.log("Call A method");
      return this.a++;
    },
    clickB: function () {
      console.log("Call B method");
      return this.b++;
    },
    submitForm() {
      const newUser = {
        name: this.name ,
        age: this.c,
        job: this.job ,
        gender: this.gender,
      }
      this.users.push(newUser);
      console.log(this.users);
    },
}
}
</script>
