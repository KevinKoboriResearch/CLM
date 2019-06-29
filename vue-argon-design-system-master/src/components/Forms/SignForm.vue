<template>
    <card type="secondary" shadow
        header-classes="bg-white pb-5"
        body-classes="px-lg-5 py-lg-5"
        class="border-0">
        <template>
            <div class="text-muted text-center mb-3">
                <small>Sign in with</small>
            </div>
            <div class="btn-wrapper text-center">
                <base-button type="neutral">
                    <img slot="icon" src="img/icons/common/github.svg">
                    Github
                </base-button>

                <base-button type="neutral">
                    <img slot="icon" src="img/icons/common/google.svg">
                    Google
                </base-button>
            </div>
        </template>
        <br>
        <template>
            <form role="form">
                <span v-if="register">
                    <div class="text-center text-muted mb-4">
                        <small>Or sign up with credentials</small>
                    </div>
                    <base-input alternative
                                class="mb-3"
                                placeholder="Name"
                                addon-left-icon="ni ni-hat-3">
                    </base-input>
                    <base-input alternative
                                class="mb-3"
                                placeholder="Email"
                                addon-left-icon="ni ni-email-83">
                    </base-input>
                    <base-input alternative
                                type="password"
                                placeholder="Password"
                                addon-left-icon="ni ni-lock-circle-open">
                    </base-input>
                    <!-- <base-input alternative
                                type="password"
                                placeholder="Repeat Password"
                                addon-left-icon="ni ni-lock-circle-open">
                    </base-input> -->
                    <div class="text-muted font-italic">
                        <small>password strength:
                            <span class="text-success font-weight-700">strong</span>
                        </small>
                    </div>
                    <base-checkbox>
                        <span>I agree with the
                            <a href="#">Privacy Policy</a>
                        </span>
                    </base-checkbox>
                        <base-button type="primary" class="my-4">Create account</base-button>
                    
                        <base-button class="my-4" @click="register=false">Login</base-button>
                    
                </span>
                <span v-else>
                    <div class="text-center text-muted mb-4">
                        <small>Or sign in with credentials</small>
                    </div>
                    <base-input alternative
                                class="mb-3"
                                placeholder="Email"
                                addon-left-icon="ni ni-email-83">
                    </base-input>
                    <base-input alternative
                                type="password"
                                placeholder="Password"
                                addon-left-icon="ni ni-lock-circle-open">
                    </base-input>
                    <base-checkbox>
                        Remember me
                    </base-checkbox>
                    <base-button type="primary" class="my-4">Sign In</base-button>
                    <base-button class="my-4" @click="register=true">Register</base-button>
                </span>
            </form>
        </template>
    </card>
</template>

<script>
export default {
  data() {
    return {
      register: false
    };
  }
};
</script>
