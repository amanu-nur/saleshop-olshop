<template>
  <div class="home">
    <Navbar />

    <!-- Breadcurmb -->
    <nav aria-label="breadcrumb">
      <div class="container">
        <ol class="breadcrumb">
          <li class="breadcrumb-item">
            <a href="../index.html"><i class="fas fa-home"></i> Home</a>
          </li>
          <li class="breadcrumb-item active" aria-current="page">
            Shopping Cart
          </li>
        </ol>
      </div>
    </nav>
    <!-- end breadcrumb -->

    <!-- Shopping Cart Section Begin -->
    <section class="shopping-cart spad">
      <div class="container">
        <div class="row text-left">
          <div class="col-lg-8">
            <div class="row">
              <div class="col-lg-12">
                <div class="cart-table">
                  <table>
                    <thead>
                      <tr>
                        <th>Image</th>
                        <th class="p-name text-center">Product Name</th>
                        <th>Price</th>
                        <th>Action</th>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <td class="cart-pic first-row">
                          <img src="img/products/product-1.jpg" />
                        </td>
                        <td class="cart-title first-row text-center">
                          <h5>Pure Pineapple</h5>
                        </td>
                        <td class="p-price first-row">Rp.110.000</td>
                        <td class="delete-item">
                          <a href="#"><i class="fas fa-trash"></i></a>
                        </td>
                      </tr>
                      <tr>
                        <td class="cart-pic first-row">
                          <img src="img/products/product-2.jpg" />
                        </td>
                        <td class="cart-title first-row text-center">
                          <h5>Pure Pineapple</h5>
                        </td>
                        <td class="p-price first-row">Rp.120.000</td>
                        <td class="delete-item">
                          <a href="#"><i class="fas fa-trash"></i></a>
                        </td>
                      </tr>
                    </tbody>
                  </table>
                </div>
              </div>
              <div class="col-lg-8">
                <h4 class="mb-4">
                  Informasi Pembeli:
                </h4>
                <div class="user-checkout">
                  <form>
                    <div class="form-group">
                      <label for="namaLengkap">Nama lengkap</label>
                      <input
                        type="text"
                        class="form-control"
                        id="namaLengkap"
                        aria-describedby="namaHelp"
                        placeholder="Masukan Nama"
                      />
                    </div>
                    <div class="form-group">
                      <label for="namaLengkap">Email Address</label>
                      <input
                        type="email"
                        class="form-control"
                        id="emailAddress"
                        aria-describedby="emailHelp"
                        placeholder="Masukan Email"
                      />
                    </div>
                    <div class="form-group">
                      <label for="namaLengkap">No. HP</label>
                      <input
                        type="text"
                        class="form-control"
                        id="noHP"
                        aria-describedby="noHPHelp"
                        placeholder="Masukan No. HP"
                      />
                    </div>
                    <div class="row">
                      <div class="col">
                        <div class="form-group">
                          <label for="namaLengkap">Kode Pos</label>
                          <input
                            type="text"
                            class="form-control"
                            id="noHP"
                            aria-describedby="noHPHelp"
                            placeholder="Masukan Kode Pos"
                          />
                        </div>
                      </div>
                      <div class="col">
                        <div class="form-group">
                          <label for="namaLengkap">Provinsi</label>
                          <input
                            type="text"
                            class="form-control"
                            id="noHP"
                            aria-describedby="noHPHelp"
                            placeholder="Masukan Provinsi"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="form-group">
                      <label for="alamatLengkap">Alamat Lengkap</label>
                      <textarea
                        class="form-control"
                        id="alamatLengkap"
                        rows="3"
                      ></textarea>
                    </div>
                  </form>
                </div>
              </div>
            </div>
          </div>
          <div class="col-lg-4">
            <div class="row">
              <div class="col-lg-12">
                <div class="proceed-checkout">
                  <ul>
                    <li class="subtotal">
                      ID Transaction <span>#SH12000</span>
                    </li>
                    <li class="subtotal mt-3">Subtotal <span>$240.00</span></li>
                    <li class="subtotal mt-3">Pajak <span>10%</span></li>
                    <li class="subtotal mt-3">
                      Total Biaya <span>Rp.131.000</span>
                    </li>
                    <li class="subtotal mt-3">Ongkir<span>COD</span></li>
                  </ul>
                  <router-link class="proceed-btn" to="/success"
                    >I ALREADY PAID</router-link
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Shopping Cart Section End -->

    <Footer />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    Footer,
  },
};

window.scrollTo(0, 0);
</script>
