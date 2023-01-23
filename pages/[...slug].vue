<template>
  <main>
    <ContentDoc>
      <template #not-found>
        <h1>Document cannot be found</h1>
      </template>
      <template #empty>
        <h4>No Content defined</h4>
        <p>This document has been intentionally left blank.</p>
        <p>You can hide this text by editing the markdown file in the `content/index.md` </p>
  
      </template>
    </ContentDoc> 
  </main>
</template>
