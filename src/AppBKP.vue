// App.vue 

<template>
  <div id="app">
    <img alt="BCO logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your BCO-Vue-App"/>
    <h1>BioCompute Object</h1>
      <biocompute />
    <h1>Employees</h1>
    <employee-form @add:employee="addEmployee" />
    <employee-table :employees="employees" class="small-container" />
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import EmployeeTable from '@/components/EmployeeTable.vue'
  import EmployeeForm from '@/components/EmployeeForm.vue'
  //import Biocompute from './componenets/Biocompute.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    EmployeeTable,
    EmployeeForm,
    //Biocompute

  },
  methods: {
    addEmployee(employee) {
      const lastId = 
        this.employees.length > 0
        ? this.employees[this.employees.length -1].id
        : 0;
      const id = lastId + 1;
      const newEmployee = { ...employee, id };
      this.employees = [...this.employees, newEmployee];
    }
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: 'Richard Hendricks',
          email: 'richard@piedpiper.com',
        },
        {
          id: 2,
          name: 'Bertram Gilfoyle',
          email: 'gilfoyle@piedpiper.com',
        },
        {
          id: 3,
          name: 'Dinesh Chugtai',
          email: 'dinesh@piedpiper.com',
        },
      ],
    }
  },
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
