<script setup>
import { ref, watchEffect } from 'vue';
import Detail from './components/Detail.vue';

const pricing = ref(null)

const ditekan = (value) => {
  pricing.value = value?.price
}

watchEffect(() => {
  ditekan()
})
</script>

<template>
  <div class="sec1">
    <Suspense>
      <template #default>
        <Detail @passing="ditekan($event)"/>
      </template>
      <template #fallback>
        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="margin: auto; background: rgba(241, 242, 243, 0); display: block;" width="200px" height="200px" viewBox="0 0 100 100" preserveAspectRatio="xMidYMid">
        <g transform="rotate(0 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.9166666666666666s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(30 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.8333333333333334s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(60 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.75s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(90 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.6666666666666666s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(120 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.5833333333333334s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(150 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.5s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(180 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.4166666666666667s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(210 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.3333333333333333s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(240 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.25s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(270 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.16666666666666666s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(300 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="-0.08333333333333333s" repeatCount="indefinite"></animate>
          </rect>
        </g><g transform="rotate(330 50 50)">
          <rect x="47" y="24" rx="3" ry="6" width="6" height="12" fill="#1d0e0b">
            <animate attributeName="opacity" values="1;0" keyTimes="0;1" dur="1s" begin="0s" repeatCount="indefinite"></animate>
          </rect>
        </g>
        </svg>
      </template>
    </Suspense>
  </div>

  <div class="sec2">
    <button class="apple-pay"> Pay</button>
    <p class="dividen"><span>Or pay with card</span></p>
    <form action="">
      <div class="shipping-information">
        <h4>Shipping information</h4>
  
          <div class="input-group email">
            <label for="email">Email</label>
            <div>
              <input type="email" class="input-model input-model-1">
            </div>
          </div>
  
          <div class="input-group address">
            <label for="email">Shipping Address</label>
            <div>
              <select  class="input-model input-model-2">
                <option value="United States">United States</option>
                <option value="Indonesia">Indonesia</option>
                <option value="London UK">London UK</option>
                <option value="Australia">Australia</option>
              </select>
            </div>
            <div>
              <input type="text" placeholder="Name" class="input-model">
            </div>
            <div>
              <input type="text" placeholder="Address" class="input-model input-model-3">
            </div>
            <small>Enter address manually</small>
          </div>
      </div>
    
      <div class="shipping-information">
        <h4>Payment Detail</h4>
  
          <div class="input-group address">
            <label for="email">Card Information</label>
            <div class="credit-card">
              <input type="number" minlength="12" maxlength="12" min ="12" max="12" placeholder="1234 1234 1234 1234" class="input-model input-model-2">
              <i><img src="https://camo.githubusercontent.com/b45d680d48b4b642b19ac7308567ea61f995a566d8b2a9165def53740574f3b5/687474703a2f2f73746f726167652e6a302e686e2f6372656469742d636172642d6c6f676f732d322e706e67" width="100"></i>
            </div>
            <div>
              <input type="text" placeholder="MM/YY" class="input-model-half half-1">
              <input type="text" placeholder="CVC" class="input-model-half half-2">
              <i><img src="https://uxwing.com/wp-content/themes/uxwing/download/e-commerce-currency-shopping/card-cvv-icon.png" width="26" alt=""></i>
            </div>
            <div>
              <input type="checkbox" name="billing" class="input-model-checkbox">
              <label for="billing" class="billing"> Billing address is same as shipping</label>
            </div>
          </div>
      </div>
      <button class="pay">Pay ${{pricing ?? ''}}</button>
    </form>
  </div>
</template>

<style scoped>


@media (min-width: 1024px) {
  .sec1 {
    height: 100vh;
    width: 50vw;
    padding:10% 25%;
  }

  .sec2 {
    height: 100vh;
    width: 50vw;
    padding:10% 25%;
    box-shadow: -5px 0px 10px rgb(237, 237, 237);
  }
}

.apple-pay {
  width: 100%;
  height: 35px;
  font-size: 18px;
  background-color: black;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
.pay {
  width: 100%;
  height: 35px;
  font-size: 14px;
  background-color: rgb(22, 23, 41);
  color: rgb(157, 158, 166);
  border: none;
  border-radius: 6px;
  font-weight: bold;
  margin-top: 20px;
  cursor: pointer;
}

.shipping-information h4 {
  margin-top: 35px;
  font-weight: bold;
  font-weight: 14px;
}

.dividen {
   width: 100%; 
   text-align: center; 
   border-bottom: 1px solid rgb(177, 177, 177); 
   line-height: 0.1em;
   margin: 35px 0 20px; 
} 

.dividen span { 
    background:#fff; 
    color: rgb(177, 177, 177);
    padding:0 10px; 
    font-size: 14px;
}

label {
  font-size: 12px;
  font-weight: bold;
  color: rgb(107, 107, 107);
}

small {
  color: rgb(125, 125, 125);
  text-decoration: underline;
  cursor: pointer;
}

.input-group {
  margin-top: 20px;
}

select {
  padding-left: 6px !important;
}

.input-model {
  width: 100%;
  height: 32px;
  border: 1.5px solid rgb(200, 200, 200);
  padding-left: 10px;
}

.input-model-half {
  width: 50%;
  height: 32px;
  border: 1.5px solid rgb(200, 200, 200);
  padding-left: 10px;
}
.input-model-checkbox{
  width: 15px;
  height: 15px;
  margin-top: 15px;
}
.billing {
  position: absolute;
  top: 13px;
  left: 20px;
}
.input-model-1 {
  border-radius: 6px;
}
.input-model-2 {
  border-top-right-radius: 6px;
  border-top-left-radius: 6px;
  border-bottom: none;
}
.input-model-3 {
  border-bottom-right-radius: 6px;
  border-bottom-left-radius: 6px;
  border-top: none;
}
.half-1 {
  border-right: none;
  border-bottom-left-radius: 6px;
}
.half-2 {
  border-bottom-right-radius: 6px;
}

i {
  position: absolute;
  right: 10px;
  top: 8px;
}
</style>
