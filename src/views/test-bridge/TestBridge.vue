<template>
  <div class="container">
    <h1> IOS / Android bridge for sending messages to JavaScript in webview</h1>
    <br>
    <p>{{AndroidMessage}}</p>
    <br>
    <button class="Android"> send message to Android </button>

    <br>
    <br>
    <br>
    <p>{{IOSMessage}}</p>
    <br>
    <button class='ios' @click="sendMStoIOS"> send message to IOS </button>

    <br>
    <br>
    <br>
    <p>{{requestMessage}}</p>
    <button @click="sendHttp"> send request </button>
    <br>
    <div>{{rspData}}</div>

  </div>
</template>
<script>
// import appMixins from "@/assets/js/appMixins.js";
// export default {
//   name: "testBridge",
//   mixins: [appMixins],
//   data() {
//     return {
//       AndroidMessage: "No message received of Android",
//       IOSMessage: "No message received of IOS",
//       requestMessage: "response is null",
//       rspData: "",
//     };
//   },
//   methods: {
//     appSendData(data) {
//       this.receive = JSON.parse(data);
//     },
//     sendMStoIOS() {
//       window.bridge.callHandler(
//         "ObjCEcho",
//         { message: "hello IOS" },
//         function responseCallback(responseData) {
//           console.log("JS received response:", responseData);
//         }
//       );
//     },

//     sendHttp() {
//       let self = this;
//       this.$axios
//         .get(
//           "api/jdong_api/v1/api.php?actions=diydata&apikeys=jdong_api&bid=4&charset=UTF8&dataform="+
//           "json&inapi=yes&modules=portal&platform=ios&swh=480x800&version=1.9.5"
//         )
//         .then(res => {
//           self.requestMessage = "response is successed";
//           self.rspData = res.data;
//           // console.log(res.data)
//         })
//         .catch(err => (self.requestMessage = "response is failed"));
//     }
//   },
//   mounted() {
//     let self = this;
//     // bridge for ios
//     function setupWebViewJavascriptBridge(callback) {
//       if (window.WebViewJavascriptBridge) {
//         return callback(WebViewJavascriptBridge);
//       }
//       if (window.WVJBCallbacks) {
//         return window.WVJBCallbacks.push(callback);
//       }
//       window.WVJBCallbacks = [callback];
//       var WVJBIframe = document.createElement("iframe");
//       WVJBIframe.style.display = "none";
//       WVJBIframe.src = "https://__bridge_loaded__";
//       document.documentElement.appendChild(WVJBIframe);
//       setTimeout(function() {
//         document.documentElement.removeChild(WVJBIframe);
//       }, 0);
//     }

//     setupWebViewJavascriptBridge(function(bridge) {
//       /* Initialize your app here */
//       window.bridge = bridge;

//       bridge.registerHandler("JsEcho", function(data, responseCallback) {
//         console.log("Js_Echo called with:", data);
//         self.IOSMessage = data;
//         responseCallback(data);
//       });

//       // bridge.callHandler('ObjCEcho', {'message':'hello IOS'}, function responseCallback(responseData) {
//       // 	console.log("JS received response:", responseData)
//       // })
//     });
//   }
// };
</script>

<style scoped lang='less'>
.container {
  padding: 10px;

  font-size: 20px;
}
h1 {
  color: skyblue;
}
.ios {
  background-image: linear-gradient(-180deg, #90f2e5 0%, #57e1c7 100%);
  box-shadow: 0 0 30px 0 rgba(87, 225, 199, 0.3);
  border-radius: 100px;
}
.Android {
  background-image: linear-gradient(-180deg, #9adaff 0%, #61b3ff 100%);
  box-shadow: 0 0 30px 0 rgba(97, 179, 255, 0.3);
  border-radius: 100px;
}
button {
  width: 200px;
  height: 40px;

  font-size: 16px;
  border-radius: 8px;
  
  color: #fff;
}

#innerSwiper .swiper-slide {
  height: 100px;
}
#innerSwiper /deep/ .swiper-pagination-bullet {
  background: pink;
}
</style>

