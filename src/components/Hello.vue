<template>
  <div class="hello">
    <h3>Create An Assignment</h3>
    <hr>
    <div class="form-group">
      <div class="row">
        <div class="col-xs-4">
        <input type="text" class="form-control" v-model="ctitle" placeholder="title">Title</input>
        </div>
        <div class="col-xs-4">
        <input type="date" class="form-control" v-model="cdate" placeholder="mm/dd/yy">Date</input>
        </div>
        <div class="col-xs-4">
        <input type="number" class="form-control" v-model="ctime" placeholde="required time">Time</input>
        </div>
      </div>
      <br>
      <div class="row">
        <div class="col-xs-12">
          <input type="textarea" class="form-control" v-model="cdes" placeholder="describe your assignment">Description</input>
        </div>  
      </div>
      <br>
      <div class="row">
        <div class="col-xs-12">
          <input type="submit" class="btn btn-info" value="Submit">
          <input class="btn btn-info" type="reset" value="Reset">
        </div>
      </div>
    </div>
    <hr>
    <div class="jumbotron">
      <div class="row">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      cdate: '',
      ctime: '0',
      ctitle: '',
      cdes: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

/*input {
  position: relative;
}*/
</style>
