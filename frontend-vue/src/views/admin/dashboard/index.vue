<script setup>
import { ref, onMounted } from "vue";
import SidebarMenu from "../../../components/SidebarMenu.vue";
import Cookies from "js-cookie";

const user = ref(null);

onMounted(() => {
  const userData = Cookies.get('user');
  if (userData) {
    user.value = JSON.parse(userData);
  }
});
</script>

<template>
  <div class="container mt-5 mb-5">
    <div class="row">
      <div class="col-md-3">
        <SidebarMenu />
      </div>

      <div class="col-md-9">
        <div class="card border-0 rounded shadow-sm">
          <div class="card-header">DASHBOARD</div>
          <div class="card-body">
            Selamat Datang, <strong>{{ user?.name }}</strong>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
