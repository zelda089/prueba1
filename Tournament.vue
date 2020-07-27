<template>
    <div>
        <div class="page-wrapper">
            <!-- ============================================================== -->
            <!-- Container fluid  -->
            <!-- ============================================================== -->
            <div class="container-fluid">
                <!-- ============================================================== -->
                <!-- Static Slider 10  -->
                <!-- ============================================================== -->
                <Header></Header>

                <div class="bg-light spacer feature20 up graphic">
                    <img class="port-image" src="@/assets/images/tenis.jpg">

                    <div class="container">
                        <!-- Row  -->
                        <div class="row justify-content-center">
                            <div class="col-md-7 text-center">
                                <h2 class="title blanc">TOURNAMENTS</h2>
                                <h6 class="blanc">Here you can find everything related to the calendar of sporting events.<br><br>

                                    Invite your friends to enjoy the tournaments and visit their statistics.<br><br>
                                </h6>
                            </div>
                        </div>


                        <center>
                            <button class="btn btn-default filter-button" data-filter="ongoing">Ongoing</button>
                            <button class="btn btn-default filter-button" data-filter="future">Future</button>
                            <button class="btn btn-default filter-button" data-filter="ended">Ended</button>
                        </center>



                        <!-- Row  -->
                        <div class="row wrap-feature-20 ">
                            <!-- Column -->
                            <div class="col-lg-6" data-aos="flip-left" data-aos-duration="1200" v-for="(key, Matches, index) in tournaments" :key="index">
                                <div class="card filter ongoing"  data-aos="zoom-in" data-aos-duration="1200">
                                    <div class="row each-item" >
                                        <div class="col-md-8" >
                                            <div class="card-body d-flex no-block">
                                                <div class="m-r-20"><img :src="key.LogoUrl" width="70" class="rounded" /></div>
                                                <div>
                                                    <h5 class="font-medium">Football Soccer</h5>
                                                    <p class="descp">Tournament Start Date<b> 15/03/2020 - 8:00pm</b></p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-md-4 text-center">
                                            <a href="javascript:void(0)" class="text-white linking bg-success-gradiant" data-toggle="modal" data-target="#mymodal1"  @click="openModal(Matches)">Matches <i class="ti-arrow-right"></i></a>

                                            <a href="javascript:void(0)" class="text-white linking bg-success-gradiant" data-toggle="modal" data-target="#mymodal2" @click="openModal(Matches)">Standings <i class="ti-arrow-right"></i></a>
                                        </div>
                                    </div>
                                </div>


                            </div>

                            <!-- Column -->
                            <!-- Column -->

                            <!-- Column -->
                            <!-- Column -->

                            <!-- Column -->
                            <!-- Column -->

                            <!-- Column -->
                        </div>
                        <!-- Row  -->
                    </div>
                </div>
                <a class="bt-top btn btn-circle btn-lg btn-info" href="#top"><i class="ti-arrow-up"></i></a>
            </div>

            <!-- ============================================================== -->
            <!-- Modals -->
            <!-- ============================================================== -->
            <!-- modals -->
            <div id="mymodal1" class="modal fade" tabindex="-1" role="dialog" aria-labelledby="myLargeModalLabel" aria-hidden="true" style="display: none;"  >
                <div class="row m-t-40"  ></div>
                <div class="modal-dialog modal-lg">
                    <div class="modal-content">
                        <div class="modal-header">
                            <h4 class="modal-title" id="myLargeModalLabel">{{ tournamentSelected.Name }}</h4>
                            <button type="button" class="close" data-dismiss="modal" aria-hidden="true">×</button>
                        </div>
                        <div class="modal-body " v-for="(key,value,index) in tournaments" :key="index" >
                            <div class="container">
                                <div class="col-lg-12 linea  "   >
                                    <h4 class="tit "> Football Soccer {{value}}</h4>
                                    <p> Round 12 Regular Season </p>

                                    <img class="sco" src="@/assets/images/score.png">
                                    <img  :src="tournamentSelected.TournamentLogo" width="70" class="iconores" />
                                    <p class="numres">04</p>
                                    <p class="texres"> </p>
                                    <p class="numresl">02</p>
                                    <p class="texresl"> </p>
                                    <p class="loi">Hours:<b>  </b> </p>
                                    <p class="reshou">Venue:<b>School gym</b></p>

                                </div>
                                <div class="col-lg-12 linea">
                                    <h4 class="tit ">Football Soccer</h4>
                                    <p>Round 12 Regular Season</p>

                                    <img class="sco" src="@/assets/images/score.png">
                                    <img src="@/assets/images/icono1.png" width="70" class="iconores" />
                                    <p class="numres">04</p>
                                    <p class="texres">Team one</p>
                                    <p class="numresl">02</p>
                                    <p class="texresl">Team two</p>
                                    <p class="loi">Hours:<b> 8:00 am</b> </p>
                                    <p class="reshou">Venue:<b>School gym</b></p>

                                </div>
                                <div class="col-lg-12 linea">
                                    <h4 class="tit ">Football Soccer</h4>
                                    <p>Round 12 Regular Season</p>

                                    <img class="sco" src="@/assets/images/score.png">
                                    <img src="@/assets/images/icono1.png" width="70" class="iconores" />
                                    <p class="numres">04</p>
                                    <p class="texres">Team one</p>
                                    <p class="numresl">02</p>
                                    <p class="texresl">Team two</p>
                                    <p class="loi">Hours:<b> 8:00 am</b> </p>
                                    <p class="reshou">Venue:<b>School gym</b></p>

                                </div>
                                <div class="col-lg-12 linea">
                                    <h4 class="tit ">Football Soccer</h4>
                                    <p>Round 12 Regular Season</p>

                                    <img class="sco" src="@/assets/images/score.png">
                                    <img src="@/assets/images/icono1.png" width="70" class="iconores" />
                                    <p class="numres">04</p>
                                    <p class="texres">Team one</p>
                                    <p class="numresl">02</p>
                                    <p class="texresl">Team two</p>
                                    <p class="loi">Hours:<b> 8:00 am</b> </p>
                                    <p class="reshou">Venue:<b>School gym</b></p>

                                </div>

                            </div>

                        </div></div>

                </div>
            </div>
        </div>
        <div id="mymodal2" class="modal fade" tabindex="-1" role="dialog" aria-labelledby="myLargeModalLabel" aria-hidden="true" style="display: none;" >
            <div class="row m-t-40"></div>
            <div class="modal-dialog modal-lg">
                <div class="modal-content" >
                    <div class="modal-header">
                        <h4 class="modal-title" >{{ tournamentSelected.Status }}</h4>
                        <button type="button" class="close" data-dismiss="modal" aria-hidden="true">×</button>
                    </div>
                    <div class="modal-body  "   >
                        <div class="container">
                            <table width="100%" border="1"   >

                                <tbody  v-for="(key,value,index) in tournaments" :key="index">




                                <tr >
                                    <th scope="col">Position {{value}}</th>
                                    <th scope="col">Team  </th>
                                    <th scope="col">Points</th>
                                    <th scope="col">Score +</th>
                                    <th scope="col">Score -</th>

                                </tr>
                                <tr >
                                    <th scope="row" >1</th>
                                    <td>{{key.Standings[0].TeamName }}</td>
                                    <td>{{key.Standings[0].Points }}</td>
                                    <td>+63</td>
                                    <td>-14</td>
                                </tr>
                                <tr>
                                    <th scope="row">2</th>
                                    <td> {{key.Standings[1].TeamName }}  </td>
                                    <td> {{key.Standings[1].Points }}</td>
                                    <td>+78</td>
                                    <td>-25</td>
                                </tr>
                                <tr>
                                    <th scope="row">3</th>
                                    <td>{{key.Standings[2].TeamName }}</td>
                                    <td> {{key.Standings[2].Points }}</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">4</th>
                                    <td>{{key.Standings[3].TeamName }}</td>
                                    <td> {{key.Standings[3].Points }}</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>
                                <tr>
                                    <th scope="row">&nbsp;</th>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                    <td>&nbsp;</td>
                                </tr>

                                </tbody>
                            </table>

                        </div></div>

                </div>
            </div>
        </div>
        <!-- ============================================================== -->
        <!-- footer -->
        <!-- ============================================================== -->
        <div class="footer4 b-t spacer">
            <div class="container">
                <div class="row">
                    <div class="col-lg-3 col-md-6 m-b-30">
                        <h5 class="m-b-20">Address</h5>
                        <p>Tel Aviv University, P.O. Box 39040, Tel Aviv 6997801, Israel</p>
                    </div>
                    <div class="col-lg-3 col-md-6 m-b-30">
                        <h5 class="m-b-20">Phone</h5>
                        <p>05 39 31 23 48</p>
                    </div>
                    <div class="col-lg-3 col-md-6 m-b-30">
                        <h5 class="m-b-20">Email</h5>
                        <p>Office :  <a href="#" class="link">info@tazuz.org</a> <br/>Site :  <a href="#" class="link">hi@tazuz.org</a></p>
                    </div>
                    <div class="col-lg-3 col-md-6">
                        <h5 class="m-b-20">Social</h5>
                        <div class="round-social light">
                            <a href="#" class="link"><i class="fa fa-facebook"></i></a>
                            <a href="#" class="link"><i class="fa fa-twitter"></i></a>
                            <a href="#" class="link"><i class="fa fa-google-plus"></i></a>
                            <a href="#" class="link"><i class="fa fa-youtube-play"></i></a>
                            <a href="#" class="link"><i class="fa fa-instagram"></i></a>
                        </div>
                    </div>
                </div>
                <div class="f4-bottom-bar">
                    <div class="row">
                        <div class="col-md-12">
                            <div class="d-flex font-14">
                                <div class="m-t-10 m-b-10 copyright">All Rights Reserved by TAZUZ.</div>
                                <div class="links ml-auto m-t-10 m-b-10">
                                    <a href="#" class="p-10 p-l-0">Terms of Use</a>
                                    <a href="#" class="p-10">Legal Disclaimer</a>
                                    <a href="#" class="p-10">Privacy Policy</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Header from "../components/Header";
    import axios from "axios";

    export default {
        components: {Header},

        name: "Tournament",

        data: () => {
            return {



                tournaments: [],

                tournamentSelected: {},
                tourSelected: {},

                tournament:'',
                tour:''
            };
        },

        mounted() {
            const university = localStorage.getItem('university');
            axios.get(`https://tazuz-d281a.firebaseio.com/${university}/Tournaments.json?auth=1DfXFRPwRe9OveIAnKiZUlzXaYb3rozZyHdD1OLA`).then((response) => {
                console.log(response.data);
                this.tournaments = response.data;


            });
        },

        methods: {
            openModal(tournament) {
                const university = localStorage.getItem('university');
                console.log(tournament);
                this.tournament = tournament;

                axios.get(`https://tazuz-d281a.firebaseio.com/${university}/Tournaments/${tournament}.json?auth=1DfXFRPwRe9OveIAnKiZUlzXaYb3rozZyHdD1OLA`).then((response) => {

                    console.log(response.data);
                    this.tournamentSelected = response.data;

                });







            }



        }



    }
</script>

<style scoped>

</style>