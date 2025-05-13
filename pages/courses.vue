<script setup lang="ts">
// const people = await $fetch('/api/courses');
const courses = [
    {
        name: "course1", 
        time: "1.30h", 
        teachers: ["teacher1", "teacher2"],
        level: "beginner",
        starting_date: "2023-10-01",
    }, 
    {
        name: "course2", 
        time: "2.30h", 
        teachers: ["teacher1", "teacher2"],
        level: "beginner",
        starting_date: "2023-10-01",
    }, 
    {
        name: "course3", 
        time: "2.30h", 
        teachers: ["teacher1", "teacher2"],
        level: "beginner",
        starting_date: "2023-10-01",
    },
    {
        name: "course4", 
        time: "2.30h", 
        teachers: ["teacher1", "teacher2"],
        level: "beginner",
        starting_date: "2023-10-01",
    }, 
    {
        name: "course4", 
        time: "2.30h", 
        teachers: ["teacher1", "teacher2"],
        level: "beginner",
        starting_date: "2023-10-01",
    }, 
    {
        name: "course4", 
        time: "2.30h", 
        teachers: ["teacher1", "teacher2"],
        level: "beginner",
        starting_date: "2023-10-01",
    } 
]
</script>

<template>
    <Breadcrumb /> 
    <div class="courses">
        <course_card v-for="course in courses" :course="course"/>
    </div>
</template>

<style scoped>
.courses{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    padding: 10px;
    gap: 20px;
}

</style>