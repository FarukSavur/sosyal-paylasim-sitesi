<template>
  <Layout>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <h1 class="my-3">Gönderiler</h1>
        </div>

        <div
          class="col-12 shadow-sm py-3 rounded bg-light mb-4"
          v-for="(post, index) in posts"
          :key="index"
        >
          <div
            class="p-2 d-flex align-items-center justify-content-between border-bottom"
          >
            <div>kullanıcı id'si {{ post.user_id }}</div>
            <div class="dropdown">
              <button
                class="btn btn-sm btn-outline-dark"
                type="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                <i class="bi bi-three-dots-vertical"></i>
              </button>
              <ul class="dropdown-menu">
                <li><button class="dropdown-item" type="button">Action</button></li>
                <li>
                  <button class="dropdown-item" type="button">Another action</button>
                </li>
                <li>
                  <button class="dropdown-item" type="button">Something else here</button>
                </li>
              </ul>
            </div>
          </div>

          <div class="p-2">
            <p>
              {{ post.content + " ***** " + post.id }}
            </p>
          </div>

          <div class="d-flex justify-content-between align-items-center border-top p-2">
            <div class="d-flex justify-content-between align-items-center gap-4">
              <div class="d-flex align-items-center justify-content-center">
                <i class="bi bi-hand-thumbs-up me-1"></i> {{ index }} beğeni
              </div>
              <div class="d-flex align-items-center justify-content-center">
                <i class="bi bi-chat-left-dots me-1"></i>{{ index }} yorum
              </div>
            </div>
            <div>
              <div class="d-flex justify-content-between align-items-center gap-2">
                <div class="fs-5"><i class="bi bi-bookmark-fill"></i></div>
                <div class="fs-5"><i class="bi bi-heart-fill text-danger"></i></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Layout>
</template>
<script>
import Layout from "../Layout/Index.vue";

export default {
  components: {
    Layout,
  },
  props: {
    posts: Object,
  },
};
</script>
