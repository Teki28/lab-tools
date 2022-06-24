<template>
  <div>
    <h1>DNA Quant Calc</h1>
    <hr>
    <el-row>
      <span>Number of samples:</span>
      <el-input-number v-model="num" @change="handleChange" :min="1"></el-input-number>
    </el-row>
    <hr>
    <el-row>
      <el-col :span="12">
        <ul>
          <li>
            <el-button type="success" plain @click="showSample" size="small">Samples</el-button>
          </li>
          <li>
            <el-button type="info" plain @click="showStd0" size="small">Standard:0</el-button>
          </li>
          <li>
            <el-button type="info" plain @click="showStd10" size="small">Standard:10</el-button>
          </li>
          <li>
            <el-button type="info" plain @click="showStd50" size="small">Standard:50</el-button>
          </li>
          <li>
            <el-button type="info" plain @click="showStd100" size="small">Standard:100</el-button>
          </li>
          <li>
            <el-button type="info" plain @click="showStd200" size="small">Standard:200</el-button>
          </li>
          <li>
            <el-button type="warning" plain @click="showBlank" size="small">Blank</el-button>
          </li>
        </ul>
      </el-col>
      <el-col :span="12">
        <div v-show="show==0">
          <h3>Samples:</h3>
          <div>
            TE:{{num*396}}ul <br>
            Papain extracted sample:4ul <br>
            Picogreen working reagent:{{num*400}}ul
          </div>

        </div>
        <div v-show="show==1">
          <h3>Standard 0:</h3>
          <div>
            TE:400ul <br>
            Picogreen:400ul
          </div>
        </div>
        <div v-show="show==2">
          <h3>Standard 10:</h3>
          <div>
            LabmdaDNA:4ul
            <br>
            TE:396 ul <br>
            Picogreen:400ul
          </div>
        </div>
        <div v-show="show==3">
          <h3>Standard 50:</h3>
          <div>
            LabmdaDNA:20ul
            <br>
            TE:380 ul <br>
            Picogreen:400ul
          </div>
        </div>
        <div v-show="show==4">
          <h3>Standard 100:</h3>
          <div>
            LabmdaDNA:40ul
            <br>
            TE:360 ul <br>
            Picogreen:400ul
          </div>
        </div>
        <div v-show="show==5">
          <h3>Standard 200:</h3>
          <div>
            LabmdaDNA:80ul
            <br>
            TE:320 ul <br>
            Picogreen:400ul
          </div>
        </div>
        <div v-show="show==6">
          <h3>Blank:</h3>
          <div>
            TE:400ul <br>
            Picogreen:400ul
          </div>
        </div>
      </el-col>
    </el-row>
    <hr>
    <h3>Total preparation:</h3>

    <h5>Picogreen working reagent: {{(num+7)*400}} ul</h5>
    <h5>Including: <br> Picogreen--- <strong>{{(num+7)*2}}ul</strong> <br>
      1*TE---<strong>{{(num+7)*398}}ul</strong> </h5>

  </div>
</template>

<script>
export default {
  data () {
    return {
      num: 1,
      show: 0
    };
  },
  methods: {
    handleChange (value) {
      console.log(value)
    },
    showSample () {
      this.show = 0
    },
    showStd0 () {
      this.show = 1
    },
    showStd10 () {
      this.show = 2
    },
    showStd50 () {
      this.show = 3
    },
    showStd100 () {
      this.show = 4
    },
    showStd200 () {
      this.show = 5
    },
    showBlank () {
      this.show = 6
    }
  }
};
</script>

<style>
ul {
  list-style: none;
}
ul li {
  margin-top: 5px;
}
</style>