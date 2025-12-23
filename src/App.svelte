<script lang="ts">
  import Header from "./lib/Header.svelte";
  import GenderForm from "./lib/GenderForm.svelte";
  import MobileNumberForm from "./lib/MobileNumberForm.svelte";
  import NationalityForm from "./lib/NationalityForm.svelte";
  import SkinComplexionForm from "./lib/SkinComplexionForm.svelte";
  import BirthMonthForm from "./lib/BirthMonthForm.svelte";
  import AgeForm from "./lib/AgeForm.svelte";
  import EmailForm from "./lib/EmailForm.svelte";
  import Footer from "./lib/Footer.svelte";
</script>

<main
  class="flex flex-col items-center justify-center gap-4 max-w-lg md:min-w-lg px-6 py-8"
>
  <Header />
  <GenderForm />
  <MobileNumberForm />
  <NationalityForm />
  <SkinComplexionForm />
  <BirthMonthForm />
  <AgeForm />
  <EmailForm />

  <button
    class="btn w-full"
    onclick={() => {
      alert("SUBMIT IT IN YOUR ASS!");
    }}>Submit</button
  >

  <Footer />
</main>
