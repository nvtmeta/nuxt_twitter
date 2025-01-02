<script setup lang="ts">
import {HomeIcon} from '@heroicons/vue/24/solid'; // For solid icons
const {defaultTransition} = useTailwindConfig()
import {
  HashtagIcon,
  BellIcon,
  InboxIcon,
  BookmarkIcon,
  DocumentTextIcon,
  UserIcon,
  PencilIcon,
  ChevronDownIcon
} from "@heroicons/vue/24/outline"

</script>

<template>
  <div class="flex flex-col h-screen">


    <div class="p-2 my-2 rounded-full hover:bg-blue-50 w-min dark:hover:bg-white/20" :class="defaultTransition">
      <nuxt-link to="/">
        <div class="w-8 h-8">
          <LogoTwitter/>
        </div>
      </nuxt-link>
    </div>


    <div class="mt-2 space-y-3">

      <SideBarLeftTab active>
        <template v-slot:icon>
          <HomeIcon/>
        </template>
        <template v-slot:name>
          Home
        </template>
      </SideBarLeftTab>

      <SideBarLeftTab>
        <template v-slot:icon>
          <HashtagIcon/>
        </template>
        <template v-slot:name>
          Explore
        </template>
      </SideBarLeftTab>


      <SideBarLeftTab>
        <template v-slot:icon>
          <BellIcon/>
        </template>
        <template v-slot:name>
          Notifications
        </template>
      </SideBarLeftTab>


      <SideBarLeftTab>
        <template v-slot:icon>
          <InboxIcon/>
        </template>
        <template v-slot:name>
          Messages
        </template>
      </SideBarLeftTab>

      <SideBarLeftTab>
        <template v-slot:icon>
          <BookmarkIcon/>
        </template>
        <template v-slot:name>
          Bookmarks
        </template>
      </SideBarLeftTab>


      <SideBarLeftTab>
        <template v-slot:icon>
          <DocumentTextIcon/>
        </template>
        <template v-slot:name>
          Lists
        </template>
      </SideBarLeftTab>


      <SideBarLeftTab>
        <template v-slot:icon>
          <UserIcon/>
        </template>
        <template v-slot:name>
          Profile
        </template>
      </SideBarLeftTab>

      <SideBarLeftTab>
        <template v-slot:icon>
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6.75 12a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0ZM12.75 12a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0ZM18.75 12a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Z" />
          </svg>
        </template>
        <template v-slot:name>
          More
        </template>
      </SideBarLeftTab>

    </div>
  </div>
</template>

<style scoped>

</style>