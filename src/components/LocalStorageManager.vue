<template>
    <div></div>
  </template>
  
  <script>
  export default {
    name: 'LocalStorageManager',
    methods: {
        saveToLocalStorage(key, data) {
        try {
            localStorage.setItem(key, JSON.stringify(data));
        } catch (error) {
            console.error('Error saving data to local storage:', error);
        }
        },
        getFromLocalStorage(key) {
        try {
            const data = localStorage.getItem(key);
            return data ? JSON.parse(data) : null;
        } catch (error) {
            console.error('Error retrieving data from local storage:', error);
            return null;
        }
    },
    },
  };
  </script>