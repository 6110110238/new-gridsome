<template>
  <Layout>
    <v-container>
      <v-row align="stretch" align-content="stretch">
        <v-col md="4" cols="12">
          <v-card class="pa-5">
            <div class="text-center">
              <v-avatar size="256" color="primary">
                <img src="https://scontent.fhdy4-1.fna.fbcdn.net/v/t1.6435-9/67299134_2272004086211022_614191851020222464_n.jpg?_nc_cat=101&ccb=1-3&_nc_sid=174925&_nc_ohc=LuSTaaglWwIAX8o4MDQ&_nc_oc=AQlCMEQa-F3CIeAxTB_Sgi-0nW65hpsKv9i2bZ7okCc-caHF8m6L0viJ-2WmyXV0g6s&_nc_ht=scontent.fhdy4-1.fna&oh=7c46d9b7cef0ca0e6306bde59917c175&oe=60FD305D" />
              </v-avatar>
            </div>
            <v-card-title class="align-end fill-height">{{aboutData.aboutMe.name}}</v-card-title>
            <v-card-text>
              <span class="font-weight-bold">{{aboutData.aboutMe.title}}</span>
              <br />
              {{aboutData.aboutMe.bio}}
            </v-card-text>
            <div class="text-center">
              <v-chip
                class="ma-1"
                color="primary"
                v-for="(item, index) in aboutData.aboutMe.hashtags"
                :key="index"
              >{{item}}</v-chip>
            </div>
          </v-card>
        </v-col>
        <v-col md="8" cols="12">
          <v-card color="accent lighten-2">
            <v-card-title
              class="display-2 align-end fill-height"
            >{{aboutData.aboutMe.long_summary_title}}</v-card-title>
            <v-card-text class="headline">{{aboutData.aboutMe.long_summary}}</v-card-text>
          </v-card>

          <v-card color="accent lighten-2">
            <v-card-title
              class="display-2 align-end fill-height"
            >{{aboutData.aboutMe.long_summary_title2}}</v-card-title>
            <v-card-text class="headline">{{aboutData.aboutMe.long_summary2}}</v-card-text>
          </v-card>

        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <Chart :skillsData="aboutData.aboutMe.skills" />
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="12">
          <div class="display-2 text-center my-5">My Developer Story</div>
          <Timeline :timeline="aboutData.aboutMe.timeline" />
        </v-col>
      </v-row>
    </v-container>
  </Layout>
</template>

<script>
import Timeline from "../components/Timeline";
import Chart from "../components/Chart";
import aboutData from "~/data/about.yml";

export default {
  components: {
    Timeline,
    Chart
  },
  data() {
    return {
      aboutData
    };
  }
};
</script>
