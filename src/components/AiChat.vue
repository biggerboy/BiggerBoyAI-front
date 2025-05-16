<template>
  <div class="layout">
    <aside :class="['sidebar', { collapsed: sidebarCollapsed }]">
      <template v-if="!sidebarCollapsed">
        <div class="sidebar-header">
          <div class="sidebar-title">BiggerSeek</div>
          <button class="sidebar-toggle-btn" @click="sidebarCollapsed = true" title="收起边栏">
            <!-- <svg width="24" height="24" viewBox="0 0 24 24"><path d="M15 19l-7-7 7-7" stroke="#888" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round"/></svg> -->
             <svg viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><defs><clipPath id="clip1382_20239"><rect id="折叠边栏0730" width="30.000000" height="30.000000" fill="white" fill-opacity="0"></rect></clipPath></defs><rect id="折叠边栏0730" width="30.000000" height="30.000000" fill="#FFFFFF" fill-opacity="0"></rect><g clip-path="url(#clip1382_20239)"><rect id="rect" x="17.420410" y="12.316406" rx="1.000947" width="5.995172" height="2.001895" transform="rotate(137.159 17.420410 12.316406)" fill="currentColor" fill-opacity="1.000000"></rect><rect id="rect" x="12.959473" y="13.728516" rx="0.995190" width="6.002943" height="1.990380" transform="rotate(40.853 12.959473 13.728516)" fill="currentColor" fill-opacity="1.000000"></rect><path id="path" d="M20.1 25.5L9.9 25.51C9.48 25.51 9.06 25.47 8.65 25.39C8.24 25.3 7.84 25.18 7.45 25.02C7.06 24.86 6.69 24.66 6.34 24.43C5.99 24.19 5.67 23.92 5.37 23.63C5.07 23.33 4.81 23 4.58 22.65C4.34 22.3 4.15 21.93 3.98 21.54C3.82 21.15 3.7 20.75 3.62 20.34C3.54 19.93 3.5 19.51 3.5 19.09L3.5 10.93C3.5 10.51 3.54 10.1 3.62 9.68C3.7 9.27 3.82 8.87 3.98 8.48C4.15 8.09 4.34 7.72 4.58 7.37C4.81 7.02 5.07 6.69 5.37 6.39C5.67 6.1 5.99 5.83 6.34 5.6C6.69 5.36 7.06 5.16 7.45 5C7.84 4.84 8.24 4.72 8.65 4.64C9.06 4.55 9.48 4.51 9.9 4.51L20.1 4.5C20.52 4.5 20.94 4.54 21.35 4.62C21.76 4.7 22.16 4.83 22.55 4.99C22.94 5.15 23.31 5.35 23.66 5.58C24 5.82 24.33 6.08 24.62 6.38C24.92 6.68 25.19 7 25.42 7.35C25.65 7.7 25.85 8.07 26.01 8.46C26.17 8.85 26.3 9.25 26.38 9.67C26.46 10.08 26.5 10.5 26.5 10.92L26.5 19.07C26.5 19.5 26.46 19.91 26.38 20.32C26.3 20.74 26.17 21.14 26.01 21.53C25.85 21.92 25.65 22.29 25.42 22.64C25.19 22.99 24.92 23.31 24.62 23.61C24.33 23.91 24 24.17 23.66 24.41C23.31 24.64 22.94 24.84 22.55 25C22.16 25.16 21.76 25.29 21.35 25.37C20.94 25.45 20.52 25.5 20.1 25.5ZM9.9 6.6C9.61 6.6 9.33 6.63 9.05 6.69C8.78 6.74 8.51 6.82 8.24 6.93C7.98 7.04 7.73 7.18 7.5 7.33C7.26 7.49 7.04 7.67 6.84 7.87C6.64 8.07 6.46 8.29 6.31 8.53C6.15 8.77 6.02 9.01 5.91 9.28C5.8 9.54 5.72 9.81 5.66 10.09C5.61 10.37 5.58 10.65 5.58 10.93L5.58 19.09C5.58 19.37 5.61 19.65 5.66 19.93C5.72 20.21 5.8 20.48 5.91 20.74C6.02 21.01 6.15 21.26 6.31 21.49C6.46 21.73 6.64 21.95 6.84 22.15C7.04 22.35 7.26 22.53 7.5 22.69C7.73 22.85 7.98 22.98 8.24 23.09C8.51 23.2 8.78 23.28 9.05 23.33C9.33 23.39 9.61 23.42 9.9 23.42L20.1 23.41C20.38 23.41 20.67 23.37 20.94 23.32C21.22 23.26 21.49 23.18 21.75 23.07C22.01 22.96 22.26 22.83 22.5 22.67C22.73 22.51 22.95 22.33 23.15 22.13C23.35 21.93 23.53 21.71 23.69 21.48C23.85 21.24 23.98 20.99 24.09 20.73C24.2 20.47 24.28 20.2 24.33 19.92C24.39 19.64 24.42 19.36 24.42 19.07L24.42 10.92C24.42 10.64 24.39 10.35 24.33 10.07C24.28 9.79 24.2 9.52 24.09 9.26C23.98 9 23.85 8.75 23.69 8.51C23.53 8.28 23.35 8.06 23.15 7.86C22.95 7.66 22.73 7.48 22.5 7.32C22.26 7.16 22.01 7.03 21.75 6.92C21.49 6.81 21.22 6.73 20.94 6.67C20.67 6.62 20.38 6.59 20.1 6.59L9.9 6.6Z" fill="currentColor" fill-opacity="1.000000" fill-rule="nonzero"></path><path id="rect" d="M8.5 5.51L10.54 5.51L10.6 24.43L8.55 24.43L8.5 5.51Z" fill="currentColor" fill-opacity="1.000000" fill-rule="evenodd"></path></g></svg>
          </button>
        </div>
        
        <div class="sidebar-newchat-btn" @click="startNewChat" title="开启新对话">
            <div class="newchat-icon">
              <svg width="28" height="28" viewBox="0 0 28 28" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M9.10999 27C8.92999 27 8.76001 26.96 8.60001 26.9C8.43001 26.83 8.29 26.74 8.16 26.61C8.03 26.49 7.94 26.3499 7.87 26.1899C7.79999 26.0299 7.76001 25.8599 7.76001 25.6899L7.73001 23.04C7.34001 22.98 6.95001 22.8799 6.57001 22.7599C6.19001 22.6299 5.83001 22.48 5.48001 22.29C5.13001 22.1 4.79999 21.88 4.48999 21.63C4.17999 21.39 3.89 21.1199 3.63 20.82C3.37 20.52 3.13999 20.21 2.92999 19.87C2.72999 19.53 2.56001 19.18 2.42001 18.82C2.28001 18.45 2.17001 18.07 2.10001 17.69C2.03001 17.3 2 16.92 2 16.53V9.46995C2 9.03995 2.04 8.61995 2.12 8.19995C2.21 7.77995 2.34 7.36995 2.5 6.96995C2.67 6.57995 2.88 6.19995 3.12 5.84995C3.36 5.48995 3.64001 5.15995 3.95001 4.85995C4.26001 4.55995 4.59999 4.28995 4.95999 4.04995C5.32999 3.80995 5.70999 3.60995 6.10999 3.44995C6.51999 3.27995 6.94 3.15995 7.37 3.07995C7.79999 2.98995 8.23001 2.94995 8.67001 2.94995H13.3C13.46 2.94995 13.61 2.97995 13.76 3.03995C13.9 3.09995 14.03 3.17995 14.14 3.28995C14.25 3.39995 14.33 3.51995 14.39 3.65995C14.45 3.79995 14.48 3.94995 14.48 4.09995C14.48 4.25995 14.45 4.39995 14.39 4.54995C14.33 4.68995 14.25 4.80995 14.14 4.91995C14.03 5.02995 13.9 5.10995 13.76 5.16995C13.61 5.22995 13.46 5.25995 13.3 5.25995H8.67001C8.38001 5.25995 8.09999 5.27995 7.82999 5.33995C7.54999 5.38995 7.27999 5.46995 7.01999 5.57995C6.75999 5.67995 6.50999 5.80995 6.26999 5.96995C6.03999 6.11995 5.82 6.29995 5.62 6.48995C5.42 6.68995 5.23999 6.89995 5.07999 7.12995C4.92999 7.35995 4.78999 7.59995 4.67999 7.85995C4.57999 8.10995 4.49 8.37995 4.44 8.64995C4.38 8.91995 4.35999 9.18995 4.35999 9.46995V16.53C4.35999 16.81 4.38 17.08 4.44 17.36C4.5 17.63 4.58 17.9 4.69 18.16C4.8 18.42 4.93 18.67 5.09 18.9C5.25 19.13 5.43001 19.3499 5.64001 19.5499C5.84001 19.75 6.05999 19.92 6.29999 20.08C6.53999 20.24 6.79 20.37 7.06 20.47C7.32 20.58 7.6 20.66 7.88 20.72C8.16001 20.77 8.44001 20.7999 8.73001 20.7999C8.91001 20.7999 9.08 20.83 9.25 20.9C9.41 20.97 9.55999 21.0599 9.67999 21.18C9.80999 21.3099 9.91001 21.45 9.98001 21.61C10.05 21.77 10.08 21.94 10.09 22.11L10.1 23.74L13.08 21.61C13.84 21.07 14.69 20.7999 15.63 20.7999H19.32C19.61 20.7999 19.89 20.77 20.16 20.72C20.44 20.67 20.71 20.59 20.97 20.4799C21.23 20.3699 21.48 20.24 21.72 20.09C21.95 19.94 22.17 19.76 22.37 19.57C22.57 19.3699 22.75 19.16 22.91 18.93C23.07 18.7 23.2 18.46 23.31 18.2C23.41 17.95 23.5 17.68 23.55 17.41C23.61 17.14 23.63 16.87 23.63 16.59V12.94C23.63 12.79 23.66 12.64 23.72 12.5C23.78 12.36 23.87 12.23 23.98 12.13C24.09 12.02 24.22 11.93 24.36 11.88C24.51 11.82 24.66 11.79 24.82 11.79C24.97 11.79 25.12 11.82 25.27 11.88C25.41 11.93 25.54 12.02 25.65 12.13C25.76 12.23 25.85 12.36 25.91 12.5C25.97 12.64 26 12.79 26 12.94V16.59C26 17.02 25.95 17.44 25.87 17.86C25.78 18.28 25.66 18.69 25.49 19.08C25.32 19.48 25.11 19.8499 24.87 20.2099C24.63 20.57 24.35 20.9 24.04 21.2C23.73 21.5 23.39 21.7699 23.03 22.0099C22.67 22.2499 22.28 22.45 21.88 22.61C21.47 22.77 21.06 22.9 20.63 22.9799C20.2 23.07 19.76 23.11 19.32 23.11H16.4C15.47 23.11 14.62 23.3799 13.86 23.9199L9.91 26.74C9.67 26.91 9.39999 27 9.10999 27Z" fill="currentColor"></path><path d="M24.6805 5.14453H18.1874C17.5505 5.14453 17.0342 5.66086 17.0342 6.29778C17.0342 6.9347 17.5505 7.45102 18.1874 7.45102H24.6805C25.3175 7.45102 25.8338 6.9347 25.8338 6.29778C25.8338 5.66086 25.3175 5.14453 24.6805 5.14453Z" fill="currentColor"></path><path d="M22.6137 3.1804C22.6137 2.52848 22.0852 2 21.4333 2C20.7814 2 20.2529 2.52848 20.2529 3.1804V9.4168C20.2529 10.0687 20.7814 10.5972 21.4333 10.5972C22.0852 10.5972 22.6137 10.0687 22.6137 9.4168V3.1804Z" fill="currentColor"></path></svg>  
            </div>
          开启新对话
        </div>
        <div class="conversation-list">
          <div
            v-for="c in conversations"
            :key="c.conversationId"
            class="conversation-item"
            :class="{ active: c.conversationId === currentConversationId }"
            @click="loadConversationMessages(c.conversationId)"
          >
            <div class="conversation-title">{{ c.title || '新对话' }}</div>
            <div class="conversation-date">{{ formatDate(c.createdAt) }}</div>
          </div>
        </div>
      </template>
      <template v-else>
        <div class="sidebar-collapsed-content">
          <button class="sidebar-toggle-btn" @click="sidebarCollapsed = false" title="展开边栏">
            <!-- <svg width="24" height="24" viewBox="0 0 24 24"><path d="M9 5l7 7-7 7" stroke="#888" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round"/></svg> -->
             <svg viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><defs><clipPath id="clip1381_20236"><rect id="打开边栏0730" width="30.000000" height="30.000000" fill="white" fill-opacity="0"></rect></clipPath></defs><rect id="打开边栏0730" width="30.000000" height="30.000000" fill="#FFFFFF" fill-opacity="0"></rect><g clip-path="url(#clip1381_20236)"><rect id="rect" x="11.572754" y="17.683594" rx="1.000947" width="5.995172" height="2.001895" transform="rotate(-42.841 11.572754 17.683594)" fill="currentColor" fill-opacity="1.000000"></rect><rect id="rect" x="16.033691" y="16.271484" rx="0.995190" width="6.002943" height="1.990380" transform="rotate(-139.147 16.033691 16.271484)" fill="currentColor" fill-opacity="1.000000"></rect><path id="path" d="M20.09 25.48L9.89 25.5C9.47 25.5 9.05 25.45 8.64 25.37C8.23 25.29 7.83 25.17 7.44 25C7.05 24.84 6.68 24.64 6.33 24.41C5.98 24.18 5.66 23.91 5.36 23.61C5.07 23.31 4.8 22.99 4.57 22.64C4.34 22.29 4.14 21.92 3.98 21.53C3.82 21.14 3.69 20.74 3.61 20.32C3.53 19.91 3.49 19.49 3.49 19.07L3.49 10.92C3.49 10.5 3.53 10.08 3.61 9.67C3.69 9.25 3.82 8.85 3.98 8.46C4.14 8.07 4.34 7.7 4.57 7.35C4.8 7 5.07 6.68 5.36 6.38C5.66 6.08 5.98 5.81 6.33 5.58C6.68 5.35 7.05 5.15 7.44 4.99C7.83 4.82 8.23 4.7 8.64 4.62C9.05 4.54 9.47 4.5 9.89 4.5L20.09 4.48C20.51 4.48 20.93 4.52 21.34 4.6C21.75 4.69 22.15 4.81 22.54 4.97C22.93 5.13 23.3 5.33 23.65 5.57C24 5.8 24.32 6.06 24.62 6.36C24.92 6.66 25.18 6.98 25.41 7.33C25.65 7.69 25.84 8.06 26.01 8.45C26.17 8.84 26.29 9.24 26.37 9.65C26.45 10.06 26.49 10.48 26.5 10.91L26.5 19.06C26.49 19.48 26.45 19.89 26.37 20.31C26.29 20.72 26.17 21.12 26.01 21.51C25.84 21.9 25.65 22.27 25.41 22.62C25.18 22.97 24.92 23.3 24.62 23.6C24.32 23.89 24 24.16 23.65 24.39C23.3 24.63 22.93 24.83 22.54 24.99C22.15 25.15 21.75 25.27 21.34 25.35C20.93 25.44 20.51 25.48 20.09 25.48ZM9.89 6.59C9.61 6.59 9.32 6.62 9.05 6.67C8.77 6.73 8.5 6.81 8.24 6.92C7.98 7.03 7.73 7.16 7.49 7.32C7.26 7.48 7.04 7.66 6.84 7.86C6.64 8.06 6.46 8.28 6.3 8.51C6.14 8.75 6.01 9 5.9 9.26C5.79 9.52 5.71 9.8 5.66 10.07C5.6 10.35 5.57 10.63 5.57 10.92L5.57 19.07C5.57 19.36 5.6 19.64 5.66 19.92C5.71 20.19 5.79 20.47 5.9 20.73C6.01 20.99 6.14 21.24 6.3 21.48C6.46 21.71 6.64 21.93 6.84 22.13C7.04 22.33 7.26 22.51 7.49 22.67C7.73 22.83 7.98 22.96 8.24 23.07C8.5 23.18 8.77 23.26 9.05 23.32C9.32 23.37 9.61 23.4 9.89 23.4L20.09 23.39C20.38 23.39 20.66 23.36 20.94 23.3C21.21 23.25 21.48 23.17 21.75 23.06C22.01 22.95 22.26 22.81 22.49 22.66C22.73 22.5 22.95 22.32 23.15 22.12C23.35 21.91 23.52 21.7 23.68 21.46C23.84 21.22 23.97 20.98 24.08 20.71C24.19 20.45 24.27 20.18 24.33 19.9C24.38 19.62 24.41 19.34 24.41 19.06L24.41 10.91C24.41 10.62 24.38 10.34 24.33 10.06C24.27 9.78 24.19 9.51 24.08 9.25C23.97 8.98 23.84 8.74 23.68 8.5C23.52 8.26 23.35 8.04 23.15 7.84C22.95 7.64 22.73 7.46 22.49 7.3C22.26 7.15 22.01 7.01 21.75 6.9C21.48 6.79 21.21 6.71 20.94 6.66C20.66 6.6 20.38 6.57 20.09 6.57L9.89 6.59Z" fill="currentColor" fill-opacity="1.000000" fill-rule="nonzero"></path><path id="rect" d="M8.49 5.5L10.53 5.5L10.59 24.41L8.54 24.41L8.49 5.5Z" fill="currentColor" fill-opacity="1.000000" fill-rule="evenodd"></path></g></svg>
          </button>
          <button class="sidebar-collapsed-newchat-btn" @click="startNewChat" title="开启新对话">
            <!-- <svg width="24" height="24" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10" fill="#eaf3ff"/><path d="M12 8v8M8 12h8" stroke="#3A8DFF" stroke-width="2" stroke-linecap="round"/></svg> -->
            <svg width="28" height="28" viewBox="0 0 28 28" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M9.10999 27C8.92999 27 8.76001 26.96 8.60001 26.9C8.43001 26.83 8.29 26.74 8.16 26.61C8.03 26.49 7.94 26.3499 7.87 26.1899C7.79999 26.0299 7.76001 25.8599 7.76001 25.6899L7.73001 23.04C7.34001 22.98 6.95001 22.8799 6.57001 22.7599C6.19001 22.6299 5.83001 22.48 5.48001 22.29C5.13001 22.1 4.79999 21.88 4.48999 21.63C4.17999 21.39 3.89 21.1199 3.63 20.82C3.37 20.52 3.13999 20.21 2.92999 19.87C2.72999 19.53 2.56001 19.18 2.42001 18.82C2.28001 18.45 2.17001 18.07 2.10001 17.69C2.03001 17.3 2 16.92 2 16.53V9.46995C2 9.03995 2.04 8.61995 2.12 8.19995C2.21 7.77995 2.34 7.36995 2.5 6.96995C2.67 6.57995 2.88 6.19995 3.12 5.84995C3.36 5.48995 3.64001 5.15995 3.95001 4.85995C4.26001 4.55995 4.59999 4.28995 4.95999 4.04995C5.32999 3.80995 5.70999 3.60995 6.10999 3.44995C6.51999 3.27995 6.94 3.15995 7.37 3.07995C7.79999 2.98995 8.23001 2.94995 8.67001 2.94995H13.3C13.46 2.94995 13.61 2.97995 13.76 3.03995C13.9 3.09995 14.03 3.17995 14.14 3.28995C14.25 3.39995 14.33 3.51995 14.39 3.65995C14.45 3.79995 14.48 3.94995 14.48 4.09995C14.48 4.25995 14.45 4.39995 14.39 4.54995C14.33 4.68995 14.25 4.80995 14.14 4.91995C14.03 5.02995 13.9 5.10995 13.76 5.16995C13.61 5.22995 13.46 5.25995 13.3 5.25995H8.67001C8.38001 5.25995 8.09999 5.27995 7.82999 5.33995C7.54999 5.38995 7.27999 5.46995 7.01999 5.57995C6.75999 5.67995 6.50999 5.80995 6.26999 5.96995C6.03999 6.11995 5.82 6.29995 5.62 6.48995C5.42 6.68995 5.23999 6.89995 5.07999 7.12995C4.92999 7.35995 4.78999 7.59995 4.67999 7.85995C4.57999 8.10995 4.49 8.37995 4.44 8.64995C4.38 8.91995 4.35999 9.18995 4.35999 9.46995V16.53C4.35999 16.81 4.38 17.08 4.44 17.36C4.5 17.63 4.58 17.9 4.69 18.16C4.8 18.42 4.93 18.67 5.09 18.9C5.25 19.13 5.43001 19.3499 5.64001 19.5499C5.84001 19.75 6.05999 19.92 6.29999 20.08C6.53999 20.24 6.79 20.37 7.06 20.47C7.32 20.58 7.6 20.66 7.88 20.72C8.16001 20.77 8.44001 20.7999 8.73001 20.7999C8.91001 20.7999 9.08 20.83 9.25 20.9C9.41 20.97 9.55999 21.0599 9.67999 21.18C9.80999 21.3099 9.91001 21.45 9.98001 21.61C10.05 21.77 10.08 21.94 10.09 22.11L10.1 23.74L13.08 21.61C13.84 21.07 14.69 20.7999 15.63 20.7999H19.32C19.61 20.7999 19.89 20.77 20.16 20.72C20.44 20.67 20.71 20.59 20.97 20.4799C21.23 20.3699 21.48 20.24 21.72 20.09C21.95 19.94 22.17 19.76 22.37 19.57C22.57 19.3699 22.75 19.16 22.91 18.93C23.07 18.7 23.2 18.46 23.31 18.2C23.41 17.95 23.5 17.68 23.55 17.41C23.61 17.14 23.63 16.87 23.63 16.59V12.94C23.63 12.79 23.66 12.64 23.72 12.5C23.78 12.36 23.87 12.23 23.98 12.13C24.09 12.02 24.22 11.93 24.36 11.88C24.51 11.82 24.66 11.79 24.82 11.79C24.97 11.79 25.12 11.82 25.27 11.88C25.41 11.93 25.54 12.02 25.65 12.13C25.76 12.23 25.85 12.36 25.91 12.5C25.97 12.64 26 12.79 26 12.94V16.59C26 17.02 25.95 17.44 25.87 17.86C25.78 18.28 25.66 18.69 25.49 19.08C25.32 19.48 25.11 19.8499 24.87 20.2099C24.63 20.57 24.35 20.9 24.04 21.2C23.73 21.5 23.39 21.7699 23.03 22.0099C22.67 22.2499 22.28 22.45 21.88 22.61C21.47 22.77 21.06 22.9 20.63 22.9799C20.2 23.07 19.76 23.11 19.32 23.11H16.4C15.47 23.11 14.62 23.3799 13.86 23.9199L9.91 26.74C9.67 26.91 9.39999 27 9.10999 27Z" fill="currentColor"></path><path d="M24.6805 5.14453H18.1874C17.5505 5.14453 17.0342 5.66086 17.0342 6.29778C17.0342 6.9347 17.5505 7.45102 18.1874 7.45102H24.6805C25.3175 7.45102 25.8338 6.9347 25.8338 6.29778C25.8338 5.66086 25.3175 5.14453 24.6805 5.14453Z" fill="currentColor"></path><path d="M22.6137 3.1804C22.6137 2.52848 22.0852 2 21.4333 2C20.7814 2 20.2529 2.52848 20.2529 3.1804V9.4168C20.2529 10.0687 20.7814 10.5972 21.4333 10.5972C22.0852 10.5972 22.6137 10.0687 22.6137 9.4168V3.1804Z" fill="currentColor"></path></svg>
          </button>
        </div>
      </template>
    </aside>
    <main class="main-content">
      <div class="chat-container" ref="messagesContainer">
        <div class="conversation-header" v-if="currentConversationId">
          <div class="conversation-header-content">
            <div class="conversation-title">{{ getCurrentConversationTitle() }}</div>
          </div>
        </div>
        <div class="chat-messages">
          <div v-if="messages.length === 0" class="welcome-message">
            <p class="welcome-message-title">
              <span class="welcome-logo">
                <svg width="36" height="36" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="24" cy="24" r="22" fill="#3A8DFF"/>
                  <rect x="14" y="18" width="20" height="14" rx="7" fill="#fff"/>
                  <ellipse cx="19.5" cy="25" rx="2.5" ry="3" fill="#3A8DFF"/>
                  <ellipse cx="28.5" cy="25" rx="2.5" ry="3" fill="#3A8DFF"/>
                  <rect x="20" y="30" width="8" height="2" rx="1" fill="#B3D1FF"/>
                  <rect x="22" y="10" width="4" height="6" rx="2" fill="#3A8DFF"/>
                </svg>
              </span>
              我是 BiggerSeek，很高兴见到你！
            </p>
            <p class="welcome-message-content">我可以帮你写代码、读文件、写作各种创意内容，请把你的任务交给我吧~</p>
            <p class="welcome-message-content">关注公众号【BiggerBoy】，获取更多技术干货~</p>
          </div>
          <div v-else v-for="(message, index) in messages" :key="index" class="message" :class="message.type">
            <img
              v-if="message.type === 'ai'"
              class="avatar"
              src="https://api.dicebear.com/7.x/bottts/svg?seed=ai"
              alt="AI"
            />
            <img
              v-if="message.type === 'user'"
              class="avatar"
              src="https://api.dicebear.com/7.x/personas/svg?seed=user"
              alt="User"
            />
            <div class="message-content-wrapper">
              <div
                class="message-content markdown-body"
                v-if="message.type === 'ai'"
                v-html="renderMarkdown(message.content)"
              ></div>
              <div
                class="message-content"
                v-if="message.type === 'user'"
              >{{ message.content }}</div>
              <button class="copy-btn" v-if="message.type === 'user'" @click="copyMessage(message.content)">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#555" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
                  <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
                </svg>
                <span class="copy-tooltip">复制</span>
              </button>
              <button class="copy-btn" v-if="message.type === 'ai' && message.done" @click="copyMessage(message.content)">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#555" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
                  <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
                </svg>
                <span class="copy-tooltip">复制</span>
              </button>
            </div>
          </div>

        </div>
        <!-- 开启新对话 -->
        <div v-if="messages.length > 0" class="start-new-chat-btn" @click="startNewChat">
            <div class="newchat-icon" title="开启新对话">
              <svg width="28" height="28" viewBox="0 0 28 28" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M9.10999 27C8.92999 27 8.76001 26.96 8.60001 26.9C8.43001 26.83 8.29 26.74 8.16 26.61C8.03 26.49 7.94 26.3499 7.87 26.1899C7.79999 26.0299 7.76001 25.8599 7.76001 25.6899L7.73001 23.04C7.34001 22.98 6.95001 22.8799 6.57001 22.7599C6.19001 22.6299 5.83001 22.48 5.48001 22.29C5.13001 22.1 4.79999 21.88 4.48999 21.63C4.17999 21.39 3.89 21.1199 3.63 20.82C3.37 20.52 3.13999 20.21 2.92999 19.87C2.72999 19.53 2.56001 19.18 2.42001 18.82C2.28001 18.45 2.17001 18.07 2.10001 17.69C2.03001 17.3 2 16.92 2 16.53V9.46995C2 9.03995 2.04 8.61995 2.12 8.19995C2.21 7.77995 2.34 7.36995 2.5 6.96995C2.67 6.57995 2.88 6.19995 3.12 5.84995C3.36 5.48995 3.64001 5.15995 3.95001 4.85995C4.26001 4.55995 4.59999 4.28995 4.95999 4.04995C5.32999 3.80995 5.70999 3.60995 6.10999 3.44995C6.51999 3.27995 6.94 3.15995 7.37 3.07995C7.79999 2.98995 8.23001 2.94995 8.67001 2.94995H13.3C13.46 2.94995 13.61 2.97995 13.76 3.03995C13.9 3.09995 14.03 3.17995 14.14 3.28995C14.25 3.39995 14.33 3.51995 14.39 3.65995C14.45 3.79995 14.48 3.94995 14.48 4.09995C14.48 4.25995 14.45 4.39995 14.39 4.54995C14.33 4.68995 14.25 4.80995 14.14 4.91995C14.03 5.02995 13.9 5.10995 13.76 5.16995C13.61 5.22995 13.46 5.25995 13.3 5.25995H8.67001C8.38001 5.25995 8.09999 5.27995 7.82999 5.33995C7.54999 5.38995 7.27999 5.46995 7.01999 5.57995C6.75999 5.67995 6.50999 5.80995 6.26999 5.96995C6.03999 6.11995 5.82 6.29995 5.62 6.48995C5.42 6.68995 5.23999 6.89995 5.07999 7.12995C4.92999 7.35995 4.78999 7.59995 4.67999 7.85995C4.57999 8.10995 4.49 8.37995 4.44 8.64995C4.38 8.91995 4.35999 9.18995 4.35999 9.46995V16.53C4.35999 16.81 4.38 17.08 4.44 17.36C4.5 17.63 4.58 17.9 4.69 18.16C4.8 18.42 4.93 18.67 5.09 18.9C5.25 19.13 5.43001 19.3499 5.64001 19.5499C5.84001 19.75 6.05999 19.92 6.29999 20.08C6.53999 20.24 6.79 20.37 7.06 20.47C7.32 20.58 7.6 20.66 7.88 20.72C8.16001 20.77 8.44001 20.7999 8.73001 20.7999C8.91001 20.7999 9.08 20.83 9.25 20.9C9.41 20.97 9.55999 21.0599 9.67999 21.18C9.80999 21.3099 9.91001 21.45 9.98001 21.61C10.05 21.77 10.08 21.94 10.09 22.11L10.1 23.74L13.08 21.61C13.84 21.07 14.69 20.7999 15.63 20.7999H19.32C19.61 20.7999 19.89 20.77 20.16 20.72C20.44 20.67 20.71 20.59 20.97 20.4799C21.23 20.3699 21.48 20.24 21.72 20.09C21.95 19.94 22.17 19.76 22.37 19.57C22.57 19.3699 22.75 19.16 22.91 18.93C23.07 18.7 23.2 18.46 23.31 18.2C23.41 17.95 23.5 17.68 23.55 17.41C23.61 17.14 23.63 16.87 23.63 16.59V12.94C23.63 12.79 23.66 12.64 23.72 12.5C23.78 12.36 23.87 12.23 23.98 12.13C24.09 12.02 24.22 11.93 24.36 11.88C24.51 11.82 24.66 11.79 24.82 11.79C24.97 11.79 25.12 11.82 25.27 11.88C25.41 11.93 25.54 12.02 25.65 12.13C25.76 12.23 25.85 12.36 25.91 12.5C25.97 12.64 26 12.79 26 12.94V16.59C26 17.02 25.95 17.44 25.87 17.86C25.78 18.28 25.66 18.69 25.49 19.08C25.32 19.48 25.11 19.8499 24.87 20.2099C24.63 20.57 24.35 20.9 24.04 21.2C23.73 21.5 23.39 21.7699 23.03 22.0099C22.67 22.2499 22.28 22.45 21.88 22.61C21.47 22.77 21.06 22.9 20.63 22.9799C20.2 23.07 19.76 23.11 19.32 23.11H16.4C15.47 23.11 14.62 23.3799 13.86 23.9199L9.91 26.74C9.67 26.91 9.39999 27 9.10999 27Z" fill="currentColor"></path><path d="M24.6805 5.14453H18.1874C17.5505 5.14453 17.0342 5.66086 17.0342 6.29778C17.0342 6.9347 17.5505 7.45102 18.1874 7.45102H24.6805C25.3175 7.45102 25.8338 6.9347 25.8338 6.29778C25.8338 5.66086 25.3175 5.14453 24.6805 5.14453Z" fill="currentColor"></path><path d="M22.6137 3.1804C22.6137 2.52848 22.0852 2 21.4333 2C20.7814 2 20.2529 2.52848 20.2529 3.1804V9.4168C20.2529 10.0687 20.7814 10.5972 21.4333 10.5972C22.0852 10.5972 22.6137 10.0687 22.6137 9.4168V3.1804Z" fill="currentColor"></path></svg>
              <span>开启新对话</span>
            </div>
            
        </div>
        <!-- 聊天输入框 -->
        <div class="chat-input-container">
          <div class="chat-input-container-wrapper">
              <div class="chat-input-row-1">
                <textarea v-model="userInput" @keyup.enter="sendMessage" placeholder="给 BiggerSeek 发送消息" :disabled="isLoading" rows="2"></textarea>
              </div>
              <div class="chat-input-row-2">
                <div class="option-buttons">
                  <button :class="['option-btn', useLocal ? 'selected' : '']" @click="useLocal = !useLocal">
                    <span class="checkbox-icon">
                      <svg width="18" height="18" viewBox="0 0 24 24" fill="none">
                        <rect x="2" y="2" width="20" height="20" rx="6" :fill="useLocal ? '#3A8DFF' : '#eaf3ff'" :stroke="useLocal ? '#3A8DFF' : '#bbb'" stroke-width="2"/>
                        <path d="M7 8.5V16a1 1 0 0 0 1 1h8" :stroke="useLocal ? '#fff' : '#bbb'" stroke-width="1.5" fill="none"/>
                        <path d="M7 8.5A2.5 2.5 0 0 1 9.5 6H17a1 1 0 0 1 1 1v9a1 1 0 0 1-1 1h-8a1 1 0 0 1-1-1V8.5z" :stroke="useLocal ? '#fff' : '#bbb'" stroke-width="1.5" fill="none"/>
                        <rect x="10" y="10" width="4" height="1" rx="0.5" :fill="useLocal ? '#fff' : '#bbb'"/>
                      </svg>
                    </span>
                    <span :style="{color: useLocal ? '#2266bb' : '#bbb'}">本地知识库</span>
                  </button>
                  <button :class="['option-btn', useWeb ? 'selected' : '']" @click="useWeb = !useWeb">
                    <span class="checkbox-icon">
                      <svg width="18" height="18" viewBox="0 0 24 24" fill="none">
                        <rect x="2" y="2" width="20" height="20" rx="6" :fill="useWeb ? '#3A8DFF' : '#eaf3ff'" :stroke="useWeb ? '#3A8DFF' : '#bbb'" stroke-width="2"/>
                        <circle cx="12" cy="12" r="5" :stroke="useWeb ? '#fff' : '#bbb'" stroke-width="1.5" fill="none"/>
                        <path d="M12 7a5 5 0 0 0 0 10" :stroke="useWeb ? '#fff' : '#bbb'" stroke-width="1.5" fill="none"/>
                        <path d="M7 12h10" :stroke="useWeb ? '#fff' : '#bbb'" stroke-width="1.5" fill="none"/>
                        <path d="M12 7a8 8 0 0 1 0 10" :stroke="useWeb ? '#fff' : '#bbb'" stroke-width="1.5" fill="none"/>
                      </svg>
                    </span>
                    <span :style="{color: useWeb ? '#2266bb' : '#bbb'}">联网搜索</span>
                  </button>
                </div>
                <button class="send-btn option-send-btn" @click="sendMessage" :disabled="isLoading || !userInput.trim()">
                  <svg v-if="!isLoading" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#fff" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M12 23V5" />
                    <path d="M5 12l7-7 7 7" />
                  </svg>
                  <svg v-else width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#fff" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
                    <rect x="5" y="5" width="14" height="14" rx="2"/>
                  </svg>
                </button>
              </div>
          </div>
          <div class="_0fcaa63">内容由 AI 生成，请仔细甄别</div>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
import { ref, onMounted, nextTick, watch } from 'vue'
import { marked } from 'marked'
import hljs from 'highlight.js'
import 'highlight.js/styles/github.css'

// 配置 marked
marked.setOptions({
  highlight: function(code, lang) {
    if (lang && hljs.getLanguage(lang)) {
      return hljs.highlight(code, { language: lang }).value
    }
    return hljs.highlightAuto(code).value
  },
  breaks: true, // 支持换行
  gfm: true, // 支持 GitHub 风格的 Markdown
})

const messages = ref([])
const userInput = ref('')
const isLoading = ref(false)
const messagesContainer = ref(null)
const useLocal = ref(false)
const useWeb = ref(false)
const requestId = ref('')
const showNewChatBtn = ref(false)

// 会话列表相关
const conversations = ref([])
const sidebarCollapsed = ref(false)
const currentConversationId = ref(null)

const fetchConversations = async () => {
  try {
    const res = await fetch('http://localhost:8080/conversations')
    const data = await res.json()
    conversations.value = data
    // 如果有当前对话ID，确保它在列表中保持高亮
    if (currentConversationId.value) {
      const exists = data.some(c => c.conversationId === currentConversationId.value)
      if (!exists) {
        currentConversationId.value = null
      }
    }
  } catch (e) {
    conversations.value = []
    currentConversationId.value = null
  }
}

const formatDate = (dateStr) => {
  const d = new Date(dateStr)
  return d.toLocaleString()
}

// Generate a unique request ID
const generateRequestId = () => {
  return 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
    const r = Math.random() * 16 | 0
    const v = c === 'x' ? r : (r & 0x3 | 0x8)
    return v.toString(16)
  })
}

const renderMarkdown = (content) => {
  return marked(content)
}

const handleScroll = () => {
  const el = messagesContainer.value
  if (!el) return
  showNewChatBtn.value = el.scrollHeight - el.scrollTop - el.clientHeight < 10
}

const startNewChat = () => {
  messages.value = []
  requestId.value = generateRequestId()
  currentConversationId.value = requestId.value // 设置当前对话ID为新生成的requestId
  showNewChatBtn.value = false
}

const scrollToBottom = async () => {
  await nextTick()
  if (messagesContainer.value) {
    messagesContainer.value.scrollTop = messagesContainer.value.scrollHeight
    // handleScroll()
  }
}

const sendMessage = async () => {
  if (!userInput.value.trim() || isLoading.value) return

  // 添加用户消息
  messages.value.push({
    type: 'user',
    content: userInput.value
  })

  const message = userInput.value
  userInput.value = ''
  isLoading.value = true

  // 添加AI消息占位
  messages.value.push({
    type: 'ai',
    content: '',
    done: false
  })

  try {
    console.log('hljs:', hljs)
    const response = await fetch(`http://localhost:8080/ai/v2/generateStream?message=${encodeURIComponent(message)}&local=${useLocal.value}&web=${useWeb.value}&requestId=${requestId.value}`, {
      headers: {
        'Accept': 'text/event-stream',
      }
    })

    const reader = response.body.getReader()
    const decoder = new TextDecoder()
    let buffer = '' // 添加缓冲区

    while (true) {
      const { done, value } = await reader.read()
      if (done) break

      const chunk = decoder.decode(value)
      buffer += chunk // 将新数据添加到缓冲区
      
      // 处理SSE格式的数据
      const lines = buffer.split('\n')
      buffer = lines.pop() || '' // 保留最后一个不完整的行

      for (const line of lines) {
        if (line.startsWith('data:')) {
          try {
            const jsonStr = line.slice(5).trim()
            if (jsonStr) {
              const data = JSON.parse(jsonStr)
              if (data.content) {
                messages.value[messages.value.length - 1].content += data.content
                await scrollToBottom()
              }
            }
          } catch (e) {
            console.error('Error parsing JSON:', e)
          }
        }
      }
    }
    // AI消息流式加载结束，done设为true
    messages.value[messages.value.length - 1].done = true
    // 刷新对话列表
    await fetchConversations()
  } catch (error) {
    console.error('Error:', error)
    messages.value[messages.value.length - 1].content = '抱歉，发生了错误，请稍后重试。'
    messages.value[messages.value.length - 1].done = true
  } finally {
    isLoading.value = false
    await scrollToBottom()
  }
}

const copyMessage = async (content) => {
  try {
    await navigator.clipboard.writeText(content)
  } catch (e) {
    alert('复制失败')
  }
}

// 加载会话消息
const loadConversationMessages = async (conversationId) => {
  try {
    const res = await fetch(`http://localhost:8080/conversationMessage/list/${conversationId}`)
    const data = await res.json()
    messages.value = data.map(item => ({
      type: item.role === 'user' ? 'user' : 'ai',
      content: item.content,
      done: item.role === 'assistant' // 只有ai消息有done
    }))
    currentConversationId.value = conversationId
    requestId.value = conversationId // 保持AI对话连续性
    await scrollToBottom()
  } catch (e) {
    messages.value = []
  }
}

onMounted(() => {
  requestId.value = generateRequestId()
  scrollToBottom()
  fetchConversations()
  nextTick(() => {
    if (messagesContainer.value) {
      messagesContainer.value.addEventListener('scroll', handleScroll)
      handleScroll()
    }
  })
})

// 自动滚动到底部
watch(messages.value, async () => {
  await nextTick()
  scrollToBottom()
}, { deep: true })

const getCurrentConversationTitle = () => {
  const conversation = conversations.value.find(c => c.conversationId === currentConversationId.value)
  return conversation ? conversation.title || '新对话' : '新对话'
}
</script>

<style>
.layout {
  display: flex;
  height: 100vh;
}
.sidebar {
  width: 260px;
  background: #f7f9fb;
  /* border-right: 1px solid #e6e6e6; */
  transition: width 0.2s;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  position: relative;
}
.sidebar.collapsed {
  width: 48px;
}
.sidebar-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 18px 16px 8px 18px;
}
.sidebar-title {
  font-size: 22px;
  font-weight: bold;
  /* color: #3A8DFF; */
  letter-spacing: 1px;
}
.sidebar-toggle-btn {
  background: #bbd4f4;
  border: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  box-shadow: 0 1px 4px rgba(0,0,0,0.06);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background 0.2s;
  /* margin-left: 8px; */
}
.sidebar-toggle-btn:hover {
  background: #eaf3ff;
}
.sidebar-newchat-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 16px 16px 16px;
  width: calc(100% - 100px);
  height: 44px;
  background: #bbd4f4;
  color: #2178f3;
  border: none;
  border-radius: 22px;
  font-size: 16px;
  font-weight: 500;
  box-shadow: 0 2px 12px rgba(58,141,255,0.08);
  cursor: pointer;
  transition: background 0.2s, color 0.2s;
}
.sidebar-newchat-btn:hover {
  background: #6ba9f6!important;
  color: #fff;
}
.conversation-list {
  flex: 1;
  overflow-y: auto;
}
.conversation-item {
  padding: 12px 16px;
  border-bottom: 1px solid #eee;
  font-size: 14px;
  cursor: pointer;
}
.conversation-item.active {
  background: #eaf3ff;
  color: #2266bb;
}
.conversation-title {
  font-weight: 600;
  color: #2266bb;
  margin-bottom: 4px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
.conversation-date {
  color: #888;
  font-size: 12px;
}
.main-content {
  flex: 1;
  min-width: 0;
}

#app {
  /* min-height: 100vh;
  display: flex; */
  width: 100%;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.chat-container {
  width: 100%;
  /* max-width: 1000px; */
  height: 100vh;
  margin: 0 auto;
  /* background: #fff;
  border-radius: 16px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.08); */
  display: flex;
  flex-direction: column;
  overflow: auto;
  position: relative;
}

.chat-messages {
  flex: 1 1 0%;
  /* overflow-y: auto; */
  /* padding: 32px 24px 16px 24px; */
  width: 100%;
    max-width: 800px;
    margin: auto;
  /* background: #f7f9fb; */
}

.message {
  margin-bottom: 18px;
  /* max-width: 90%; */
  display: flex;
  align-items: flex-start;
}

.message.user {
  flex-direction: row-reverse;
}

.message.user .message-content {
  background: #007bff;
  color: white;
  text-align: right;
  /* width: 0; */
}

.message.ai {
  margin-right: auto;
}

.message-content-wrapper {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.message-content {
  /* width: 700px; */
  /* max-width: 95%; */
  min-height: 32px;
  
  border-radius: 18px;
  display: inline-block;
  font-size: 16px;
  /* box-shadow: 0 1px 4px rgba(0,0,0,0.03); */
  /* background: #fff; */
  /* border: 1px solid #e6e6e6; */
  word-break: break-word;
}

.ai .message-content {
  padding-left: 12px;
  /* background: #fff; */
  /* border: 1px solid #ddd; */
  color: #222;
}
.user .message-content {
  color: #fff;
  padding: 12px 18px;
}
.avatar {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  object-fit: cover;
  background: #eee;
  box-shadow: 0 1px 4px rgba(0,0,0,0.04);
}
.user .avatar{
  margin:  0 12px;
}

.copy-btn {
  position: relative;
  margin: 3px 5px 1px auto;
  display: block;
  background: #f5f4f4;
  border: none;
  border-radius: 4px;
  padding: 2px;
  cursor: pointer;
  opacity: 0.6;
  transition: opacity 0.2s, background 0.2s;
}
.copy-btn:hover {
  opacity: 1;
  background-color: #e6f0ff !important;
}
.copy-btn svg {
  display: block;
}
.copy-tooltip {
  display: none;
  position: absolute;
  bottom: 120%;
  left: 50%;
  transform: translateX(-50%);
  background: #222;
  color: #fff;
  padding: 2px 8px;
  border-radius: 4px;
  font-size: 12px;
  white-space: nowrap;
  pointer-events: none;
  opacity: 0;
  transition: opacity 0.2s;
  z-index: 99;
}
.copy-btn:hover .copy-tooltip {
  display: block;
  opacity: 1;
}



button {
  /* padding: 12px 28px; */
  background: #007bff;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 16px;
  transition: background 0.2s;
}

button:disabled {
  background: #9a9999;
  cursor: not-allowed;
}

button:hover:not(:disabled) {
  background: #0056b3;
}

/* Markdown 样式 */
.markdown-body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
  line-height: 1.6;
  word-wrap: break-word;
}

.markdown-body :deep(pre) {
  background-color: #f6f8fa;
  border-radius: 6px;
  padding: 16px;
  overflow: auto;
}

.markdown-body :deep(code) {
  font-family: SFMono-Regular, Consolas, "Liberation Mono", Menlo, monospace;
  font-size: 85%;
  padding: 0.2em 0.4em;
  margin: 0;
  background-color: rgba(27, 31, 35, 0.05);
  border-radius: 3px;
}

.markdown-body :deep(pre code) {
  padding: 0;
  margin: 0;
  background-color: transparent;
  border: 0;
  word-break: normal;
  white-space: pre;
}

.markdown-body :deep(p) {
  margin-top: 0;
  margin-bottom: 16px;
}

.markdown-body :deep(h1),
.markdown-body :deep(h2),
.markdown-body :deep(h3),
.markdown-body :deep(h4),
.markdown-body :deep(h5),
.markdown-body :deep(h6) {
  margin-top: 24px;
  margin-bottom: 16px;
  font-weight: 600;
  line-height: 1.25;
}

.markdown-body :deep(ul),
.markdown-body :deep(ol) {
  padding-left: 2em;
  margin-top: 0;
  margin-bottom: 16px;
}

.markdown-body :deep(table) {
  border-spacing: 0;
  border-collapse: collapse;
  margin-top: 0;
  margin-bottom: 16px;
}

.markdown-body :deep(table th),
.markdown-body :deep(table td) {
  padding: 6px 13px;
  border: 1px solid #dfe2e5;
}

.markdown-body :deep(table tr) {
  background-color: #fff;
  border-top: 1px solid #c6cbd1;
}

.markdown-body :deep(table tr:nth-child(2n)) {
  background-color: #f6f8fa;
}

.markdown-body :deep(blockquote) {
  padding: 0 1em;
  color: #6a737d;
  border-left: 0.25em solid #dfe2e5;
  margin: 0 0 16px 0;
}

.markdown-body :deep(img) {
  max-width: 100%;
  box-sizing: content-box;
  background-color: #fff;
}
.send-btn{
  width: 36px;
  height: 36px;
  border-radius: 20px;
  margin: 12px 0;
}

.welcome-message {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: #555;
  font-size: 20px;
  text-align: center;
  opacity: 0.85;
  user-select: none;
}
.welcome-message-title{
  font-size: 24px;
  font-weight: 400;
  color: #222;
  display: flex;
  align-items: center;
  gap: 10px;
}
.welcome-logo {
  display: inline-flex;
  align-items: center;
  margin-right: 6px;
}
.welcome-message-content{
  font-size: 16px;
  color: #555;
}
.chat-input-container{
  background: linear-gradient(to bottom, transparent 0%, transparent 30%, var(--dsr-bg) 30%, var(--dsr-bg) 100%);
    z-index: 7;
    flex-direction: column;
    align-items: center;
    margin-top: auto;
    display: flex;
    position: -webkit-sticky;
    position: sticky;
    bottom: 0;
}
.chat-input-container-wrapper{
  background-color: var(--dsr-input-bg);
  border-radius: 20px;
  width: 100%;
  max-width: 800px;
}
._0fcaa63{
  font-size: 12px;
    color: rgb(163 163 163);
    margin: 6px 0;
    line-height: 14px;
}
.chat-input-row-1 {
  width: 100%;
  margin-bottom: 6px;
}
.chat-input-row-2 {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  margin: 10px;
}
.option-buttons {
  display: flex;
  gap: 10px;
  margin: 0;
}
.option-send-btn {
  margin-left: auto;
  height: 36px;
  width: 36px;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #007bff;
  color: white;
  border: none;
  cursor: pointer;
  transition: background 0.2s;
}
.option-send-btn:disabled {
  background: #9a9999;
  cursor: not-allowed;
}
.option-send-btn:hover:not(:disabled) {
  background: #0056b3;
}
.option-btn {
  display: flex;
  align-items: center;
  background: #f4f8fe;
  border: 1.5px solid #e0eaff;
  color: #bbb;
  border-radius: 20px;
  padding: 4px 16px;
  font-size: 15px;
  font-weight: 400;
  cursor: pointer;
  transition: background 0.2s, border 0.2s, color 0.2s;
  outline: none;
  min-width: 110px;
}
.option-btn.selected {
  background: #eaf3ff;
  border: 1.5px solid #3A8DFF;
  color: #2266bb;
}
.option-btn svg {
  flex-shrink: 0;
}
.checkbox-icon {
  display: flex;
  align-items: center;
  margin-right: 6px;
}
.option-btn:hover{
  background: #d7e5f8!important;
}


.chat-input-row-1 {
  display: flex;
  gap: 12px;
  padding: 5px;
  /* background-color: transparent; */
  border-radius: 20px;
  border: 0;
  box-sizing: border-box;
}

textarea {
  flex: 1;
  padding: 12px;
  border: 0;
  border-radius: 20px;
  font-size: 16px;
  background-color: transparent;
  resize: none;
  font-family: inherit;
  word-break: break-word;
}

textarea:focus {
  outline: none;
  box-shadow: none;
  border-color: #ddd;
}
body{
  --dsr-main: #4d6bfe;
    --dsr-main-2: rgba(77, 107, 254, .4);
    --dsr-main-3: rgba(77, 107, 254, .2);
    --dsr-bg: rgb(var(--ds-rgb-white));
    --dsr-text-0: rgb(var(--ds-rgb-black));
    --dsr-text-1: rgb(var(--ds-rgb-neutral-800));
    --dsr-text-2: rgb(var(--ds-rgb-neutral-600));
    --dsr-text-3: rgb(var(--ds-rgb-neutral-400));
    --dsr-text-4: rgb(var(--ds-rgb-zinc-350));
    --dsr-border-1: rgb(var(--ds-rgb-neutral-350));
    --dsr-border-2: rgb(var(--ds-rgb-neutral-200));
    --dsr-input-border: #dce0e9;
    --dsr-input-bg: rgb(var(--ds-rgb-gray-100));
    --dsr-button-main-bg: var(--dsr-main);
    --dsr-button-main-bg-hover: #4166d5;
    --dsr-button-second-bg: var(--dsr-main-3);
    --dsr-button-grey-0: rgb(var(--ds-rgb-neutral-150));
    --dsr-button-grey-1: rgb(var(--ds-rgb-neutral-100));
    --dsr-button-grey-2: rgb(var(--ds-rgb-neutral-50));
    --dsr-delete-button-bg: rgb(var(--ds-rgb-red-500) / .85);
    --dsr-delete-button-bg-hover: rgb(var(--ds-rgb-red-550));
    --dsr-tooltip-fg: #eff6ff;
    --dsr-tooltip-bg: rgb(var(--ds-rgb-neutral-850));
    --dsr-side-bg: #f9fbff;
    --dsr-side-hover-bg-rgb: 239, 246, 255;
    --dsr-side-hover-bg: rgb(var(--ds-rgb-blue-50));
    --dsr-icon-fg-1: rgb(var(--ds-rgb-neutral-650));
    --dsr-icon-hover-0: rgb(var(--ds-rgb-neutral-150));
    --dsr-icon-hover-1: rgb(var(--ds-rgb-neutral-100));
    --dsr-side-icon-hover: rgb(var(--ds-rgb-slate-100));
    --dsr-error-fg: rgb(var(--ds-rgb-red-550));
    --dsr-risk-text: #e4773d;
    --dsr-risk-border: rgba(228, 119, 61, .1);
    --dsr-risk-fill: rgba(228, 119, 61, .05);
}

:root, page {
    --ds-rgb-black: 0 0 0;
    --ds-rgb-white: 255 255 255;
    --ds-rgb-slate-50: 248 250 252;
    --ds-rgb-slate-100: 241 245 249;
    --ds-rgb-slate-150: 233 238 244;
    --ds-rgb-slate-200: 226 232 240;
    --ds-rgb-slate-250: 214 222 232;
    --ds-rgb-slate-300: 203 213 225;
    --ds-rgb-slate-350: 175 188 204;
    --ds-rgb-slate-400: 148 163 184;
    --ds-rgb-slate-450: 124 139 161;
    --ds-rgb-slate-500: 100 116 139;
    --ds-rgb-slate-550: 85 100 122;
    --ds-rgb-slate-600: 71 85 105;
    --ds-rgb-slate-650: 61 75 95;
    --ds-rgb-slate-700: 51 65 85;
    --ds-rgb-slate-750: 40 53 72;
    --ds-rgb-slate-800: 30 41 59;
    --ds-rgb-slate-850: 22 32 50;
    --ds-rgb-slate-900: 15 23 42;
    --ds-rgb-slate-950: 2 6 23;
    --ds-rgb-gray-50: 249 250 251;
    --ds-rgb-gray-100: 243 244 246;
    --ds-rgb-gray-150: 236 237 240;
    --ds-rgb-gray-200: 229 231 235;
    --ds-rgb-gray-250: 219 222 227;
    --ds-rgb-gray-300: 209 213 219;
    --ds-rgb-gray-350: 182 188 197;
    --ds-rgb-gray-400: 156 163 175;
    --ds-rgb-gray-450: 131 138 151;
    --ds-rgb-gray-500: 107 114 128;
    --ds-rgb-gray-550: 91 99 113;
    --ds-rgb-gray-600: 75 85 99;
    --ds-rgb-gray-650: 65 75 90;
    --ds-rgb-gray-700: 55 65 81;
    --ds-rgb-gray-750: 43 53 68;
    --ds-rgb-gray-800: 31 41 55;
    --ds-rgb-gray-850: 24 32 47;
    --ds-rgb-gray-900: 17 24 39;
    --ds-rgb-gray-950: 3 7 18;
    --ds-rgb-zinc-50: 250 250 250;
    --ds-rgb-zinc-100: 244 244 245;
    --ds-rgb-zinc-150: 236 236 238;
    --ds-rgb-zinc-200: 228 228 231;
    --ds-rgb-zinc-250: 220 220 223;
    --ds-rgb-zinc-300: 212 212 216;
    --ds-rgb-zinc-350: 186 186 193;
    --ds-rgb-zinc-400: 161 161 170;
    --ds-rgb-zinc-450: 137 137 146;
    --ds-rgb-zinc-500: 113 113 122;
}

.start-new-chat-btn {
  /* display: flex;
  margin: 16px auto 0 auto;
  margin-bottom: 20px;
  padding: 10px;
  height: 46px;
  width: calc(10%);
  background: #b7d0f4;
  color: #455fef;
  border: none;
  border-radius: 22px;
  font-size: 16px;
  font-weight: 400;
  box-shadow: 0 2px 12px rgba(58,141,255,0.12);
  cursor: pointer;
  transition: background 0.2s; */
  justify-content: center;
    gap: 20px;
    display: flex
;
}
.start-new-chat-btn .newchat-icon:hover {
  background: #6ba9f6;
  color: #fff;
}
.start-new-chat-btn .newchat-icon{
  margin-bottom: 20px;
  padding: 10px;
  height: 46px;
  background: #b7d0f4;
  border: none;
  border-radius: 22px;
}
.newchat-icon{
  display: flex;
  margin-right: 9px;
}

.sidebar-collapsed-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 18%;
  gap: 18px;
}
.sidebar-collapsed-newchat-btn {
  background: #bbd4f4;
  color: #2178f3;
  border: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 8px;
  cursor: pointer;
  transition: background 0.2s;
}
.sidebar-collapsed-newchat-btn:hover {
  background: #6ba9f6 !important;
  color: #fff;
}

.conversation-header {
  position: sticky;
  top: 0;
  background: var(--dsr-bg);
  border-bottom: 1px solid var(--dsr-border-2);
  z-index: 10;
  padding: 12px 0;
}

.conversation-header-content {
  max-width: 800px;
  margin: 0 auto;
  padding: 0 24px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.conversation-id-label {
  color: var(--dsr-text-2);
  font-size: 14px;
}

.conversation-id-value {
  color: var(--dsr-text-1);
  font-size: 16px;
  font-weight: 600;
  background: var(--dsr-button-grey-1);
  padding: 2px 8px;
  border-radius: 4px;
  margin: auto;
}

.copy-conversation-id-btn {
  background: none;
  border: none;
  padding: 4px;
  cursor: pointer;
  color: var(--dsr-text-3);
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s;
}

.copy-conversation-id-btn:hover {
  background: var(--dsr-button-grey-1);
  color: var(--dsr-text-1);
}

.copy-conversation-id-btn svg {
  width: 16px;
  height: 16px;
}

.conversation-title {
  font-size: 16px;
  font-weight: 600;
  color: var(--dsr-text-1);
  background: var(--dsr-button-grey-1);
  padding: 2px 8px;
  border-radius: 4px;
  margin: auto;
}

</style> 