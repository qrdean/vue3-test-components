<template>
<!-- Maybe have a picture of the book -->
    <div>{{ bookObject.lccn }}</div>
    <div>{{ bookObject.isbn }}</div>
    <div>{{ bookObject.title }}</div>
    <div>{{ bookObject.author }}</div>
    <div>{{ bookObject.publishDate }}</div>
    <div>{{ bookObject.checkedIn }}</div> 
    <!-- Can Click this ^ and make call -->
</template>

<script>
export default {
    props: {
        bookObject: Object
    }
}
</script>