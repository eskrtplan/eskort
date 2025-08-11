<template>
    <div class="grid place-items-center">
       <h2>Hello World!</h2>
       <BaseBtn
       label="Primary"
       variant="primary"
       />

       <SecondaryBtn
       label="Secondary"
       variant="gold"
       />

       <TextLink
       label="Text link"
       variant="Red"
       to=""
       />

       <HistoryRdBtn
       variant="small rounded button"
       icon="uil:history"
       :notification="true"
       />

       <HistoryRdBtn
       variant="large rounded button"
       icon="uil:location"
       :notification="false"
       />

       <BaseInput
       label="Personal Information"
       placeholder="Firstname"
       variant="red icon"
       icon="uil:history"
       />

       <BaseInput
       type="number"
       placeholder="Phone number"
       variant="red icon"
       icon="uil:history"
       />

       <SearchInput
       type="search"
       placeholder="Search..."
       variant="red icon"
       icon="material-symbols:sort-rounded"
       />

       <NavLinks
       icon="ic:outline-dynamic-feed"
       title="Feeds"
       :countmssg="true"
       />

       <NavLinks
       icon="ic:outline-dynamic-feed"
       title="Feeds"
       />
       
    </div>
</template>

<script setup>
import BaseBtn from '~/components/buttons/BaseBtn.vue';
import HistoryRdBtn from '~/components/buttons/roundedBtn/RoundedBtn.vue';
import SecondaryBtn from '~/components/buttons/SecondaryBtn.vue';
import TextLink from '~/components/buttons/TextLink.vue';
import BaseInput from '~/components/inputs/BaseInput.vue';
import SearchInput from '~/components/inputs/search/SearchInput.vue';
import NavLinks from '~/components/naviagation/NavLinks.vue';
</script>