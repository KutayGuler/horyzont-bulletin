<script>
  import "../app.css";
</script>

<div class="navbar bg-base-100">
  <div class="flex-1">
    <a href="/" class="btn btn-ghost normal-case text-xl"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        fill="currentColor"
        class="w-6 h-6"
      >
        <path
          d="M19.006 3.705a.75.75 0 00-.512-1.41L6 6.838V3a.75.75 0 00-.75-.75h-1.5A.75.75 0 003 3v4.93l-1.006.365a.75.75 0 00.512 1.41l16.5-6z"
        />
        <path
          fill-rule="evenodd"
          d="M3.019 11.115L18 5.667V9.09l4.006 1.456a.75.75 0 11-.512 1.41l-.494-.18v8.475h.75a.75.75 0 010 1.5H2.25a.75.75 0 010-1.5H3v-9.129l.019-.006zM18 20.25v-9.565l1.5.545v9.02H18zm-9-6a.75.75 0 00-.75.75v4.5c0 .414.336.75.75.75h3a.75.75 0 00.75-.75V15a.75.75 0 00-.75-.75H9z"
          clip-rule="evenodd"
        />
      </svg>
    </a>
  </div>
  <div class="flex-none">
    <ul class="menu menu-horizontal p-0">
      <li><a href="/publikacje">Publikacje</a></li>
      <li><a href="/recenzje">Recenzje</a></li>
      <label for="my-modal-3" class="btn">Kontakt</label>
    </ul>
  </div>
</div>

<!-- The button to open modal -->

<!-- Put this part before </body> tag -->
<input type="checkbox" id="my-modal-3" class="modal-toggle" />
<div class="modal">
  <div class="modal-box relative">
    <label for="my-modal-3" class="btn btn-sm btn-circle absolute right-2 top-2"
      >✕</label
    >
    <h3 class="text-lg font-bold">
      Wydawnictwo Wrocławskiej Wyższej Szkoły Informatyki Stosowanej
    </h3>
    <p class="py-4">ul. ks. Marcina Lutra 4 54-239 Wrocław</p>
    <p>tel./fax: 71 799 19 37</p>
    <p>tel./fax: 71 788 94 25</p>
    <!-- TODO: LINK -->
    <p>
      e-mail: <a class="link" href="mailto:wydawnictwo@horyzont.eu"
        >wydawnictwo@horyzont.eu</a
      >
    </p>
  </div>
</div>

<slot />
