<template>
<div class="main-wrapper">
    <div class="preloader">
        <div class="lds-ripple">
            <div class="lds-pos"></div>
            <div class="lds-pos"></div>
        </div>
    </div>
  <div class="auth-wrapper d-flex no-block justify-content-center align-items-center" :style="`background:url(${require('@/assets/admin/assets/images/big/auth-bg.jpg')}) no-repeat center center;`">
      <div class="auth-box">
          <div id="loginform">
              <div class="logo">
                  <span class="db"><img src="@/assets/admin/assets/images/logo-icon.png" alt="logo" /></span>
                  <h5 class="font-medium m-b-20">Sign In to Admin</h5>
              </div>
              <!-- Form -->
              <div class="row">
                  <div class="col-12">
                      <form class="form-horizontal m-t-20" id="loginform" action="index.html">
                          <div class="input-group mb-3">
                              <div class="input-group-prepend">
                                  <span class="input-group-text" id="basic-addon1"><i class="ti-user"></i></span>
                              </div>
                              <input type="text" class="form-control form-control-lg" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
                          </div>
                          <div class="input-group mb-3">
                              <div class="input-group-prepend">
                                  <span class="input-group-text" id="basic-addon2"><i class="ti-pencil"></i></span>
                              </div>
                              <input type="text" class="form-control form-control-lg" placeholder="Password" aria-label="Password" aria-describedby="basic-addon1">
                          </div>
                          <div class="form-group text-center">
                              <div class="col-xs-12 p-b-20">
                                  <button class="btn btn-block btn-lg btn-info" type="submit">Log In</button>
                              </div>
                          </div>
                      </form>
                          <div class="form-group text-center">
                              <div class="col-xs-12 p-b-20">
                                <a href="#" style="text-decoration: none; color: whitesmoke;"><button class="btn btn-block btn-lg btn-success">Create An Account</button></a>
                              </div>
                          </div>
                          <div class="form-group text-left">
                              <div class="col-xs-12 p-b-20">
                                  <a href="/" style="text-decoration: none; color: whitesmoke;"><button class="btn btn-block btn-lg btn-danger">Back</button></a>
                              </div>
                          </div>
                  </div>
              </div>
          </div>
      </div>
  </div>
</div>
</template>