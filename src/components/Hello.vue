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
    <div class="jumbotron" v-for="item in items">
      <div class="row">
        <div class="col-xs-2 userinfo">
          <img src="http://p1.qqyou.com/touxiang/UploadPic/2015-6/19/2015061914564960842.jpeg" class="avatar img-circle img-responsive" />
          <p class="text-center">
            <strong>{{ username }}</strong>
          </p>
        </div>
        <div class="col-xs-2 timeinfo">
          <h3>
            <i class="glyphicon glyphicon-time">
            </i>
            {{ item.usertime }}
          </h3>
          <p class="label label-success text-center">
            <i class="glyphicon glyphicon-calendar"></i>
            {{ item.userdate }}
          </p>
        </div>
        <div class="col-xs-8 desinfo">
          <h3>{{ item.usertitle }}</h3>
          <p>{{ item.userdes }}</p>
        </div>
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
      cdes: '',
      username: 'Yan',
      items: [
        {
          usertime: '3',
          userdate: '2017-04-20',
          userdes: 'Finishing 5 questions in Dynamic Programming',
          usertitle: 'leetcode'
        },
        {
          usertime: '5',
          userdate: '2017-04-20',
          userdes: 'Prepare the presentation of open source project',
          usertitle: 'Presentation'
        }
      ]
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

.avatar {
  height: 100px;
  margin: 0 auto;
}

.userinfo {
  border-right: 1px solid #ddd;
  margin: -10px 0;
}
.desinfo {
  word-wrap: break-word; 
  word-break: normal; 
  margin-top:-3%;
}
.jumbotron {
  margin: 0px;
  border-bottom: 1px solid #ddd;
  padding-left:2%;
  padding-bottom: 2%;
}

</style>
