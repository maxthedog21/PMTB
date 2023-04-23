<template>
  <v-app>
    <v-main>
      <Header title="ParadymeUI" version="Beta V1"></Header>
      <v-row style="margin: 0px 0 0 0">
        <div
          style="
            width: 30%;
            background-color: #f2f2f2;
            padding: 10px;
            height: 100vh;
          "
        >
          <v-card style="height: 100%">
            <v-tabs v-model="tab" fixed-tabs color="black" class="pm-tabs">
              <!-- Tab1 -->
              <v-tab value="one">
                <div style="display: flex; align-items: center">
                  <span style="text-transform: none"
                    >Base
                    <img
                      src="./assets/images/base.png"
                      style="
                        margin-right: 10px;
                        height: 18px;
                        margin-bottom: -4px;
                      "
                  /></span>
                </div>
              </v-tab>
              <!-- Tab2 -->
              <v-tab value="two">
                <div style="display: flex; align-items: center">
                  <span style="text-transform: none"
                    >Features
                    <img
                      src="./assets/images/components.png"
                      style="
                        margin-right: 10px;
                        height: 24px;
                        margin-bottom: -7px;
                        margin-top: -5px;
                      "
                  /></span>
                </div>
              </v-tab>
              <!-- Tab3 -->
              <v-tab value="three">
                <div style="display: flex; align-items: center">
                  <span style="text-transform: none"
                    >Code
                    <img
                      src="./assets/images/code.png"
                      style="
                        margin-right: 10px;
                        height: 24px;
                        margin-bottom: -7px;
                        margin-top: -5px;
                      "
                  /></span>
                </div>
              </v-tab>
            </v-tabs>
            <v-card-text>
              <v-window v-model="tab">
                <!-- Tab1: Base -->
                <v-window-item value="one">
                  <v-row class="pt-6">
                    <v-col class="clearCSS pt-0 pb-0" cols="8" md="8">
                      <PMAutocomplete
                        :items="['CBS', 'FBI', 'New Sheet']"
                        :label="'Application Theme'"
                      ></PMAutocomplete>
                    </v-col>
                    <v-col class="pt-0 pb-0" cols="12" md="12">
                      <PMTextField
                        :label="'Title'"
                        :placeholder="'Type in the title of the application'"
                      ></PMTextField>
                      <PMTextField
                        :label="'Sub-title'"
                        :placeholder="'Type in the sub-title of the application'"
                      ></PMTextField>
                    </v-col>
                    <!-- Number of Pages -->
                    <v-col class="pt-0 pb-0 mt-5" cols="4" md="4">
                      <PMAutocomplete
                        :items="[1, 2, 3, 4, 5, 6, 7]"
                        :label="'Pages'"
                      ></PMAutocomplete>
                    </v-col>
                  </v-row>
                  <v-row class="pt-0">
                    <v-col class="pt-0 pb-0 pr-1" cols="2" md="2">
                      <PMTextField
                        :label="''"
                        :placeholder="'Image'"
                      ></PMTextField>
                    </v-col>
                    <v-col class="pt-0 pb-0 pl-0" cols="10" md="10">
                      <PMTextField
                        :label="''"
                        :placeholder="'Requests'"
                      ></PMTextField>
                    </v-col>
                  </v-row>

                  <v-row class="pt-0">
                    <v-col class="pt-0 pb-0 pr-1" cols="2" md="2">
                      <PMTextField
                        :label="''"
                        :placeholder="'Image'"
                      ></PMTextField>
                    </v-col>
                    <v-col class="pt-0 pb-0 pl-0" cols="10" md="10">
                      <PMTextField
                        :label="''"
                        :placeholder="'Jobs'"
                      ></PMTextField>
                    </v-col>
                  </v-row>

                  <v-row class="pt-0 mt-7">
                    <!-- Number of Roles -->
                    <v-col class="pt-0 pb-0" cols="4" md="4">
                      <PMAutocomplete
                        :items="[1, 2, 3, 4, 5, 6, 7]"
                        :label="'Roles'"
                      ></PMAutocomplete>
                    </v-col>
                    <v-col class="pt-0 pb-0" cols="12" md="12">
                      <PMTextField
                        :label="''"
                        :placeholder="'Role1'"
                      ></PMTextField>
                      <PMTextField
                        :label="''"
                        :placeholder="'Role2'"
                      ></PMTextField>
                    </v-col>
                  </v-row>

                  <v-row class="pt-0 mt-7">
                    <!-- Number of Rows -->
                    <v-col class="pt-0 pb-4" cols="4" md="4">
                      <PMAutocomplete
                        :items="[1, 2, 3, 4, 5, 6, 7]"
                        :label="'Rows'"
                      ></PMAutocomplete>
                    </v-col>

                    <v-col class="pt-0 pb-0" cols="12" md="12">
                      <v-row class="pt-0">
                        <v-col class="pt-0 pb-0 pr-1" cols="2" md="2">
                          <PMTextField
                            :label="''"
                            :placeholder="'1'"
                          ></PMTextField>
                        </v-col>
                        <v-col class="pt-0 pb-0 pl-0" cols="10" md="10">
                          <PMTextField
                            :label="''"
                            :placeholder="'12'"
                          ></PMTextField>
                        </v-col>
                      </v-row>

                      <v-row class="pt-0">
                        <v-col class="pt-0 pb-0 pr-1" cols="2" md="2">
                          <PMTextField
                            :label="''"
                            :placeholder="'1'"
                          ></PMTextField>
                        </v-col>
                        <v-col class="pt-0 pb-0 pl-0" cols="10" md="10">
                          <PMTextField
                            :label="''"
                            :placeholder="'12'"
                          ></PMTextField>
                        </v-col>
                      </v-row>

                      <v-row class="pt-0">
                        <v-col class="pt-0 pb-0 pr-1" cols="2" md="2">
                          <PMTextField
                            :label="''"
                            :placeholder="'1'"
                          ></PMTextField>
                        </v-col>
                        <v-col class="pt-0 pb-0 pl-0" cols="10" md="10">
                          <PMTextField
                            :label="''"
                            :placeholder="'12'"
                          ></PMTextField>
                        </v-col>
                      </v-row>
                    </v-col>
                  </v-row>
                </v-window-item>
                <!-- Tab2: Components -->
                <v-window-item value="two">
                  <v-row class="pt-6">
                    <v-col class="clearCSS pt-0 pb-0" cols="8" md="8">
                      <PMAutocomplete
                        :items="['CBS', 'FBI', 'New Sheet']"
                        :label="'Application Theme'"
                      ></PMAutocomplete>
                    </v-col>
                  </v-row>
                </v-window-item>
                <!-- Tab3: Code -->
                <v-window-item value="three"> </v-window-item>
              </v-window>
            </v-card-text>
          </v-card>
        </div>

        <!-- Screen Emulator -->
        <v-col cols>
          <PMHeader title="title" role="role" subTitle="subTitle" />
          <v-btn
            color="#212121"
            style="
              position: fixed;
              right: 2%;
              bottom: 2%;
              color: white;
              width: 135px;
              height: 45px;
              font-size: 16px;
              text-transform: none;
              letter-spacing: 0px;
            "
          >
            Download
            <img
              src="./assets/images/download.png"
              style="
                margin-left: 5px;
                height: 21px;
                margin-bottom: -6px;
                margin-top: -5px;
              "
            />
          </v-btn>
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>
<script setup>
import { ref } from "vue";
import Header from "./components/Header.vue";
import PMAutocomplete from "./features/PMAutocomplete.vue";
import PMTextField from "./features/PMTextField.vue";
import PMHeader from "./features/PMHeader.vue";
</script>
<script>
export default {
  components: {
    PMAutocomplete,
    PMTextField,
    PMHeader,
  },
  data: () => ({
    tab: null,
    title: null,
    subTitle: null,
  }),
};
</script>
<style lang="scss">
.v-window {
  min-height: 90vh !important;
}
.label span {
  color: black !important;
}

.logo.vite:hover {
  filter: drop-shadow(0 0 2em #747bff);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #249b73);
}
</style>
