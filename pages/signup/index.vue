<template>
   
   <v-app id="inspire">
    <v-main>
        <v-container fluid fill-height>
            <v-layout align-center justify-center>
                <v-flex xs12 sm8 md4>
                    <v-card class="elevation-12">

                        <v-toolbar dark color="red" >
                            <v-toolbar-title>Signup form</v-toolbar-title>
                        </v-toolbar>
                        
                        <v-card-text>
                            <v-form>
    

                                    <v-text-field
                                    name="firstName"
                                    label="firstName"
                                    type="text"
                                    v-model="firstName"     
                                    ></v-text-field>

                                    
                                    <v-text-field
                                    name="lastName"
                                    label="lastName"
                                    type="text"
                                    v-model="lastName"     
                                    ></v-text-field>

                                    <v-text-field
                                    name="email"
                                    label="Email"
                                    type="text"
                                    v-model="email"     
                                    ></v-text-field>

                                    <v-text-field
                                    id="password"
                                    name="password"
                                    label="Password"
                                    type="password"
                                    v-model="password"     
                                    ></v-text-field>
                            </v-form>
                        </v-card-text>
                        <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn color="red" @click="loginHandler">Signup</v-btn>
                        </v-card-actions>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>
    </v-main>
   </v-app>

</template>

<script>
export default {
     name:'Signup',
     data() {
        return {
            firstName : null,
            lastName : null,
            email:null,
            password : null
            }
     },
     methods: {
        loginHandler() {
            const signup = {
                'first_name' : this.firstName,
                'last_name' :this.lastName,
                'email' : this.email,
                'password' : this.password
            }
            console.log(signup);
        }
     }
}
</script>

<style scoped>
</style>