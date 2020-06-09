<template>
  <v-app>
    <v-content>
      <v-container>
        <v-row>
          <v-col class="d-inline-flex">
          <p class="display-4 font-weight-black red--text text--darken-4 mr-4">Oscar Baracos</p>
          <v-btn fab icon x-large color="red darken-4" href="https://github.com/Oscbacon">
            <v-icon x-large>fab fa-github</v-icon>
          </v-btn>
          <v-btn fab icon x-large color="red darken-4" href="https://www.linkedin.com/in/oscar-baracos-102ba4145/">
            <v-icon x-large>fab fa-linkedin-in</v-icon>
          </v-btn>
          </v-col>
        </v-row>
      <v-container>
      </v-container>
        <v-row>
          <v-col>
            <h1 class="display-2 font-weight-black red--text text--darken-4 mr-4">Experiences</h1>
          </v-col>
        </v-row>
        <v-row>
          <v-col md="9" sm="12">
            <v-timeline dense align-top>
              <v-timeline-item v-for="exp in experiences" :key="exp" color="red darken-4">
                  <h2 class="headline font-weight-bold red--text text--darken-4" v-text="exp.title"/>
                  <p class="subtitle-1">{{ exp.location }} &#8211; {{ exp.time }}</p>
                  <div>
                    <ul v-for="point in exp.description" :key="point">
                      <li v-html="point"/>
                    </ul>
                  </div>
              </v-timeline-item>
            </v-timeline>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      experiences: [
        {
          title: "Intel - Software Development Internship",
          location: "Toronto, Canada",
          time: "April 2020-Present",
        },
        {
          title: "Numberly – Backend Developer Internship",
          location: "Paris, France",
          time: "June-August 2019",
          description: [
            "Created <b>xUnit</b> test framework for <b>Tartiflette</b> (<b>GraphQL</b> framework) and <b>ScyllaDB</b> using <b>PyTest</b> and <b>AioHTTP</b> (see <a href='https://github.com/OscBacon/pytest-graphql'>GitHub</a>)",
            "Carried out internal API migration from <b>PyMSSQL</b> to <b>PyODBC</b> with low downtime",
            "Developed internal backend APIs with <b>Scylla</b>, <b>GraphQL</b>, <b>Flask</b>",
            "Containerized <b>Python</b> APIs with <b>Docker</b> and <b>Kubernetes</b>, increasing their availability",
          ],
        },
        {
          title: "Sqreen – Python Backend Software Engineer Internship",
          location: "Paris, France",
          time: "June-July 2018",
          description: [
            "Automated logging GitHub Pull Requests to a Google Sheet using <b>AWS Lambda</b> and <b>AWS Gateway API</b> (see <a href='https://github.com/OscBacon/PushPRToGoogleSheet'>GitHub</a>)",
            "Implemented <b>API endpoints</b> in <b>Flask</b> to communicate with <b>DynamoDB</b> and <b>MongoDB</b>",
            "Found and removed legacy code, refactored code for better legibility",
            "Improved documentation for clarity",
          ],
        },
        {
          title: "杭州诚道科技股份有限公司(Hangzhou Trustway Technology co., LTD)",
          location: "Hangzhou, China",
          time: "July 2017",
          description: [
            "Created a <a href='https://tw-login-demo.herokuapp.com/'>login</a> page based on a design mockup, using <b>Ruby on Rails</b> to connect to the company <b>Oracle Database</b> (see online version, using Heroku and PostgreSQL, and a mock database)",
            "Followed a MOOC in Chinese to learn <b>Java</b> basics (imooc.com, <a href='https://www.imooc.com/learn/124'>Java 入门第二季</a>)",
            "Helped implement a <b>tree structure</b> to manage office hierarchies in <b>Java</b> with a page to CRUD offices stored in an <b>Oracle Database</b>, and displaying the hierarchy for selection",
          ],
        },
      ],
    };
  },
};
</script>

<style>
a {
  color: #B71C1C!important;
  text-decoration: none;
}

a:hover {
  text-decoration: underline!important;
}

a.v-btn:hover {
  text-decoration: none!important;
}
</style>
