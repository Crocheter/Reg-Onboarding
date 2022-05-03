<template>
  <div class="row d-flex">
    <div class="first-page col-5">
      <img src="./assets/bg.png" alt="Background" class="img-fluid Bg">
    </div>
    <div class="container col-7" v-if="pageChange===true">
      <h6 class="reg-link text-end mt-5 me-4">Already have an account? <span>Sign In</span></h6>
      <div class="form">
        <div class="heading">
          <h1>Join Us!</h1>
          <p>To begin this journey, tell us what type of account you'd be opening.</p>
        </div>
        <div class="buttons">
          <button class="pt-3 mb-5 d-flex">
            <img src="./assets/user.png" alt="" class="user img-fluid">
            <img src="./assets/BluePolygon.png" alt="" class="Bp img-fluid">
            <div class="Individual text-start" @click="regOn(pageChange=false)">
              <h6 style="font-size: 16px; font-weight: 500;">
                Individual
              </h6>
              <div class="d-flex">
                <p style="color: #8692A6; font-size: 14px;">Personal account to manage all you activities.</p>
                <img src="./assets/arrow-right.png" alt="" class="Arrow-right img-fluid">
              </div>
            </div>
          </button>

          <button class="pt-3 d-flex">
            <img src="./assets/briefcase.png" alt="" class="briefcase img-fluid">
            <img src="./assets/WhitePolygon.png" alt="" class="Wp img-fluid">
            <div class="Individual text-start">
              <h6 style="font-size: 16px; font-weight: 500;"> 
                Business
              </h6>
              <p style="color: #8692A6; font-size: 14px; width: 250px">Own or belong to a company, this is for you.</p>
            </div>
          </button>
        </div>
      </div>
    </div>


    <div class="container second-page col-7 mt-5" id="page-two" v-if="false">
      <header>
        <div class="d-flex justify-content-between">
          <div class="d-flex" @click="regOn(pageChange=true)">
            <img src="./assets/arrow-back.png" alt="" class="Arrow-back img-fluid"><h6 style="color: #8692A6; font-weight: 600;"
            class="mx-2">
              Back</h6>
          </div>
        <h6 style="color: #BDBDBD; font-weight: 500;" class="me-5">STEP 01/03</h6>
        </div>
        <div class="text-end me-5" style="color: #8692A6; font-weight: 600;">Personal Info.</div>
        
      </header>
      <form action="" class="mt-5">
        <div>
          <h1 style="font-size: 27px; font-weight: 700;">Register Individual Account!</h1>
          <p style="color: #8692A6; width: 314px;">For the purpose of industry regulation, your details are required.</p>
        </div>

        <div class="form-group mt-4 mb-3">
          <label for="name">Your fullname*</label>
          <input
            type="text"
            id="name"
            class="form-control"
            placeholder="Abisola Odutayo"
          />
        </div>
        <div class="form-group mb-3">
          <label for="email">Email address*</label>
          <input
            type="email"
            id="email"
            class="form-control"
            placeholder="Enter email address"
          />
        </div>
        <div class="form-group mb-3">
          <label for="password">Create password*</label>
          <input
            type="password"
            id="password"
            class="form-control"
            placeholder="Enter password"
          />
        </div>

        <div class="form-check mb-3">
                <input class="form-check-input" type="checkbox" value="Agreement" id="Agreement">
                <label class="form-check-label" for="Agreements">
                    I agree to terms & conditions
                </label>
        </div>

        <div>
          <button style="background-color: #1565D8; width: 426px; height: 64px; color: #FFFFFF; border-radius: 5px; border: none;" 
          class="mb-3" onclick="profileOn()">Register Account</button>
          <h6 style="color: #BABABA; font-size: 10px;" class="text-center">Or</h6>
          <button style="display: block; background-color: #FFFFFF; box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.08);
          border: none; width: 426px; height: 64px;" class="d-flex align-items-center">
            <img src="./assets/google.png" alt="" class="mx-4">
            <h6 class="mx-5">Register with Google</h6>

            </button>
        </div>


      </form>
    </div>

    <div class="third-page col-7 container mt-5" id="showThird" v-if="false">
      <header>
        <div class="d-flex justify-content-between">
        <div class="d-flex">
          <img src="./assets/arrow-back.png" alt="" class="Arrow-back">
          <h6 style="color: #8692A6; font-weight: 600;"
            class="mx-2">Back</h6>
        </div>
        <h6 style="color: #BDBDBD; font-weight: 500;" class="me-4">STEP 02/03</h6>
        </div>
        <div class="text-end me-4" style="color: #8692A6; font-weight: 600;">Residency Info.</div>
        
      </header>

      <form class="mt-5">
      <div>
          <h1 style="font-size: 27px; font-weight: 700;">Complete Your Profile!</h1>
          <p style="color: #8692A6; width: 314px;">For the purpose of industry regulation, your details are required.</p>
      </div>
      <div class="form-group mb-3 mt-3">
          <label for="number">Phone number</label>
          <div class="d-flex">
            <img src="./assets/Group.svg" alt="">
              <select name="number-codes" id="nom" style="border: none;">
                <option value="rigatoni">Rigatoni</option>
                <option value="dave">Dave</option>
                <option value="pumpernickel">Pumpernickel</option>
                <option value="reeses">Reeses</option>
              </select>
            <input
              type="text"
              id="address"
              class="form-control"
              placeholder="08012345678"
            />
          </div>
        </div>

        <!-- <div class="form-group">
          <label for="number">Phone number</label>
          <select name="number-codes" id="nom">
            <option value="rigatoni">Rigatoni</option>
            <option value="dave">Dave</option>
            <option value="pumpernickel">Pumpernickel</option>
            <option value="reeses">Reeses</option>
          </select>
          <img src="./assets/naija.png" alt="">
          <input type="text" class="form-control" aria-label="Text input with dropdown button">
        </div> -->
        <div class="form-group mb-3">
          <label for="address">Your address</label>
          <input
            type="text"
            id="address"
            class="form-control"
            placeholder="Please enter address"
          />
        </div>

        <div class="form-group mb-4">
          <label for="country">Country of Residence</label>
          <input
            type="text"
            id="country"
            class="form-control"
            placeholder="Please select"
          />
        </div>
        <button style="width: 425px; border: none; background-color: #1565D8; color: #FFFFFF;
        height: 45px; border-radius: 5px;" class="mb-4">Save & Continue</button>
          <h6 class="lock text-center" style="font-size: 10px; color: #8692A6;">
          <img src="./assets/lock.png" alt="">Your Info is safely secured</h6>
      </form>
    </div>
    
    <div class="fourth-page container col-7" v-if="true">
       <header>
        <div class="d-flex justify-content-between mt-5">
        <h6 style="color: #8692A6; font-weight: 600;"><img src="./assets/arrow-back.png" alt="">Back</h6>
        <h6 class="me-4" style="color: #BDBDBD; font-weight: 500;">STEP 03/03</h6>
        </div>
        <div class="text-end me-4" style="color: #8692A6; font-weight: 600;">Bank Verification</div>
        
      </header>

      <form class="mt-5">
        <div>
          <h1>Complete Your Profile!</h1>
          <p>For the purpose of industry regulation, your details are required.</p>
        </div>
        <div class="form-group mb-3">
          <label for="country">Bank Verification Number(BVN)</label>
          <input
            type="number"
            id="bvn"
            class="form-control"
            placeholder="0123456789"
          />
        </div>
        <button style="width: 425px; border: none; background-color: #1565D8; color: #FFFFFF;
        height: 45px; border-radius: 5px;" class="mb-4">Save & Continue</button>
        <h6 class="lock text-center" style="font-size: 10px; color: #8692A6;"><img src="./assets/lock.png" alt="">Your Info is safely secured</h6>
      </form>

    </div>
  </div>
</template>

<style scoped>

/* first-page */
.reg-link {
  color: #8692A6;
  font-weight: 400;
  font-size: 15px;
}

.reg-link span {
  color: #1565D8;
  font-weight: 500;
}

.form {
  margin-left: 98px;
  margin-top: 100px;
}

.heading h1 {
  font-weight: 700;
  font-size: 30px;
}

.heading p {
  color: #8692A6;
  font-size: 16px;
  width: 350px;
}

.buttons button {
  display: block;
  background-color: #FFFFFF;
  box-shadow: 0px 2px 14px 1px rgba(0, 0, 0, 0.06);
  border-radius: 7px;
  border: none;
  height: 100px;
  width: 411px;
}

.buttons button:hover {
  border: 1px solid #1565D8;
  background-color: #F5F9FF;
  box-shadow: 0px 4px 14px 1px rgba(0, 0, 0, 0.04);
}

.Bp, .Wp {
  position: absolute;
  margin-left: 15px;
}

.user, .briefcase {
  margin-top: 17px;
  margin-left: 29px;
  position: relative;
  z-index: 2;
}

.Individual, .Business {
  margin-left: 40px;
}

.Arrow-right {
  width: 37px;
  height: 24px;
  margin-right: 10px;
}

.Bg {
  width: 100%;
  height: 100%;
}

form {
  width: 450px;
  margin-left: 79px;
}

.Arrow-back {
  height: 15px;
  width: 11px;
}

.form-group input{
  border: 1px solid #8692A6;
  border-radius: 6px;
  height: 50px;
  width: 426px;
}

.form-group input:hover {
  border: 1px solid #1565D8;
  box-shadow: 0px 4px 10px 3px rgba(0, 0, 0, 0.11);
  border-radius: 6px;
}



</style>

<script>
export default {
  data() {
    return {
      pageChange: false,
      // showThird: true
    }
  },

  methods: {
         regOn(){
           
         },
        //  profileOn(){

        //  }
       }
}

function profileOn() {
            document.getElementById('showThird').style.display='block';
            
        }
</script>