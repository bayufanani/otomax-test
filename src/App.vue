<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import sidebar from './components/sidebar.vue'
</script>

<template>
  <div class="columns">
    <div class="column is-2">
      <sidebar />
    </div>
    <div class="column is-10 ml-2">
      <div class="tabs is-boxed pt-2">
        <ul>
          <li class="is-active">
            <a><span>Transaksi</span></a>
          </li>
          <li>
            <a><span>Administrasi</span></a>
          </li>
          <li>
            <a><span>Setting</span></a>
          </li>
        </ul>
      </div>
      <div class="tabs is-boxed is-small">
        <ul>
          <li class="is-active">
            <a><span>Transaksi</span></a>
          </li>
          <li>
            <a><span>Inbox</span></a>
          </li>
          <li>
            <a><span>Outbox</span></a>
          </li>
          <li>
            <a><span>Pendaftaran</span></a>
          </li>
          <li>
            <a><span>Mutasi Saldo</span></a>
          </li>
          <li>
            <a><span>Mutasi Unit</span></a>
          </li>
          <li>
            <a><span>Transaksi Manual</span></a>
          </li>
          <li>
            <a><span>Cek Harga Grup</span></a>
          </li>
          <li>
            <a><span>Cek Harga Reseller</span></a>
          </li>
        </ul>
      </div>
      <div class="box has-background-primary-light has-text-primary p-2">Jika Auto Refresh terpilih, maka data di
        bawah
        ini
        akan
        diupdate
        secara
        realtime pada saat ada perubahan data.</div>
      <form action="">
        <table class="no-border">
          <tr>
            <td class="is-size-7">Tgl. Transaksi / Unit Data</td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>/</td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>/</td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>
              <div class="control">
                <label class="checkbox">
                  <input type="checkbox">
                  Outbox
                </label>
              </div>
            </td>
          </tr>
          <tr>
            <td class="is-size-7">Reseller / Produk / Tujuan</td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>/</td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>/</td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
          </tr>
          <tr>
            <td class="is-size-7">Modul / Status</td>
            <td colspan="3">
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>/</td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
            <td>
              <div class="control">
                <input class="input is-small" type="text">
              </div>
            </td>
          </tr>
        </table>
      </form>
      <div class="px-2 trx">
        <table class="table is-bordered is-fullwidth mt-2 is-hoverable">
          <tr>
            <th>TrxID</th>
            <th>Tgl. Entri</th>
            <th>Produk</th>
            <th>Tujuan</th>
            <th>Pengirim</th>
            <th>Modul</th>
            <th>Status</th>
            <th>Tgl. Status</th>
            <th>Hrg. Beli</th>
            <th>Hrg. Jual</th>
            <th>Jawaban Provider</th>
          </tr>
          <tr v-for="n in 20">
            <td>TrxID</td>
            <td>Tgl. Entri</td>
            <td>Produk</td>
            <td>Tujuan</td>
            <td>Pengirim</td>
            <td>Modul</td>
            <td>Status</td>
            <td>Tgl. Status</td>
            <td>Hrg. Beli</td>
            <td>Hrg. Jual</td>
            <td>Jawaban Provider</td>
          </tr>
        </table>
      </div>
      <div class="is-flex is-flex-direction-row is-justify-content-space-between py-2 ml-2">
        <div>
          <label class="checkbox mr-4">
            <input type="checkbox">
            Autosize Baris
          </label>
          <label class="checkbox mr-4">
            <input type="checkbox">
            Auto Refresh
          </label>
          <div class="select is-small">
            <select>
              <option>Medium</option>
              <option>High</option>
            </select>
          </div>
        </div>
        <div>
          <button class="button is-primary is-small mr-2">Kirim Ulang transaksi modul IM Hybrid yang pending</button>
          <button class="button is-primary is-small mr-2">Jalankan</button>
          <button class="button is-primary is-small mr-2">F5 - Refresh</button>
        </div>
      </div>
    </div>
  </div>
</template>

