<template>

    <div class="container" >
    <div class="row">
        <div v-for="item in Mu" :key="item" class="col-md-3 col-6 my-1">
            <div class="card=auto">
                <img :src="item.pic" class="card-img-top">
                <div class="card-body">
                    <div class="card-title"><h3>{{ item.name }} </h3></div>
                    <div>
                        <h5>{{item.price}} ฿
                        <button type="button" class="btn btn-success" value="item.price">เพิ่มลงในตะกร้า</button></h5>

                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

   
</template>
<script>
import axios from "axios";
import Mu from "@/store/Testsystem.json";
export default {
  data: () => ({
    Mu: Mu
  })
};
{}
</script>
<style>
.container {
  margin: 40px;
  min-height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro",-apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.card {
  width: 300px;
  height: 300px;
  margin: 10px;
  padding: 18px;
  display: inline-block;
  vertical-align: top;
}
</style>
