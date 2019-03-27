<template>
  <nav
    class="navbar default-layout-navbar col-lg-12 col-12 p-0 fixed-top d-flex flex-row"
  >
    <div
      class="text-center navbar-brand-wrapper d-flex align-items-center justify-content-center"
    >
      <NLink to="/" class="navbar-brand brand-logo">
        <img src="images/logo.svg" alt="logo" />
      </NLink>
      <NLink to="/" class="navbar-brand brand-logo-mini">
        <img src="images/logo-mini.svg" alt="logo" />
      </NLink>
    </div>

    <div class="navbar-menu-wrapper d-flex align-items-stretch">
      <b-navbar-nav class="ml-auto">
        <b-nav-item-dropdown class="nav-profile">
          <!-- Using button-content slot -->
          <template slot="button-content">
            <div class="nav-profile-img">
              <img src="images/faces/face1.jpg" alt="image" />
              <span class="availability-status online"></span>
            </div>
            <div class="nav-profile-text">
              <p class="mb-1 text-black">David Greymaax</p>
            </div>
          </template>
          <b-dropdown-item to="/log"
            ><i class="mdi mdi-cached mr-2 text-success"></i> Activity
            Log</b-dropdown-item
          >
          <b-dropdown-divider></b-dropdown-divider>
          <b-dropdown-item to="/logout"
            ><i class="mdi mdi-logout mr-2 text-primary"></i>
            Logout</b-dropdown-item
          >
        </b-nav-item-dropdown>
        <b-nav-item to="/logout" class="nav-logout d-none d-lg-block">
          <i class="mdi mdi-power"></i>
        </b-nav-item>
      </b-navbar-nav>
      <b-button
        class="navbar-toggler navbar-toggler-right d-lg-none align-self-center"
        @click="sidebarToggled"
      >
        <span class="mdi mdi-menu"></span>
      </b-button>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    sidebarToggled() {
      const el = document.querySelector('.sidebar-offcanvas')
      el.classList.toggle('active')
    }
  }
}
</script>
