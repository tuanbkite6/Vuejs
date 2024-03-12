<template>
  <section>
    <div class="row">
        <table border="1">
            <tr>
                    <th>User name</th>
                    <th>Age</th>
                    <th>Job</th>
                    <th>Gender</th>
                </tr>
                <tr class="list" v-for="user in users" :key="user">
                    <td>{{ user.name }}</td>
                    <td>{{ user.age }}</td>
                    <td>{{ user.job }}</td>
                    <td> {{ user.gender }}</td>
                </tr>
        </table>
    </div>

  </section>
</template>
<script>
export default {
  name: "InformationList",
  props : {
    users : Array
  },
};
</script>
