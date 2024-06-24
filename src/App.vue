<script setup>
import {  RouterView } from 'vue-router'
//import NavItem from './components/NavItem.vue'
  import ModalButton from './components/modal.vue';
  // import Navbar from './components/Navbar.vue';
  import NavItem from './components/NavItem.vue';
</script>


<template>
  <!-- <Navbar /> -->

  <div class="container">
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Navbar</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
    <RouterLink class="nav-link" to="/home">Home</RouterLink>
</li>
            <li class="nav-item">
    <RouterLink class="nav-link" to="/getdatamovie">Get Data Movie</RouterLink>
</li>
            <NavItem kelas="nav-link" link="/about" label="About"></NavItem>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                Profile
              </a>

              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Visi Misi</a></li>
                <li><a class="dropdown-item" href="#">Aktifitas</a></li>
                <li><hr class="dropdown-divider" /></li>
                <!-- ini batass -->

                <li><a class="dropdown-item" href="#">Tujuan</a></li>
              </ul>
            </li>
          </ul>
          <form class="d-flex" role="search">
            <input
              class="form-control me-2"
              type="search"
              placeholder="Search"
              aria-label="Search"
            />
            <button class="btn btn-outline-success" type="submit">Search</button>
          </form>
        </div>
      </div>
    </nav>

    <div class="row">
      <div class="col-12"><img src="@/assets/patung.jpg" class="img-fluid" /></div>
    </div>

    <div class="row">
      <div class="col-4">
        <div class="list-group">
          <a href="#" class="list-group-item list-group-item-action active" aria-current="true">
            The current link item
          </a>
          <a href="#" class="list-group-item list-group-item-action">A second link item</a>
          <a href="#" class="list-group-item list-group-item-action">A third link item</a>
          <a href="#" class="list-group-item list-group-item-action">A fourth link item</a>
          <a class="list-group-item list-group-item-action disabled" aria-disabled="true"
            >A disabled link item</a
          >
        </div>
      </div>

      <div class="col-8"><RouterView></RouterView></div>
    </div>
    <div class="row">
      <div class="col-12">
        <div class="col-4">
          <div class="card text-bg-primary mb-3" style="width: 100%">
            <div class="card-header">Header</div>
            <div class="card-body">
              <p class="card-text">
                Some quick example text to build on the card title and make up the bulk of the
                card's content.
              </p>
            </div>
          </div>
        </div>
        <div class="col-4">
          <div class="card text-bg-danger mb-3" style="width: 100%">
            <div class="card-header">Header</div>
            <div class="card-body">
              <p class="card-text">
                Some quick example text to build on the card title and make up the bulk of the
                card's content.
              </p>
            </div>
          </div>
        </div>
        <div class="col-4">
          <div class="card text-bg-info mb-3" style="width: 100%">
            <div class="card-header">Header</div>
            <div class="card-body">
              <p class="card-text">
                Some quick example text to build on the card title and make up the bulk of the
                card's content.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
    <div>
      <ModalButton></ModalButton>
    </div>
  
  </template>
   
