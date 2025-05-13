<script setup>
defineProps(['course'])
</script>

<template>
    <div class="course_card">
        <div class="img_course_card">
            <picture>
                <source media="(max-width:300px)" :srcset="course.img">
                <img src="~/public/defaults/image_not_found.png" width="400">
            </picture>
        </div>
        <div class="description_course_card">
            <div id="course_name">{{ course.name }}</div>
            <div id="course_time">{{ course.time }}</div>
            <div class="course_teachers">
                <div class="teacher_picture" v-for="teacher in course.teachers" :key="teacher">
                    <picture>
                        <source media="(max-width:200px)" :srcset="teacher.img">
                        <img src="~/public/defaults/image_not_found.png" width="60">
                    </picture>
                </div>
            </div>
            <div class="bottom_course_card">
                <div>level: {{ course.level }}</div>
                <div>{{ course.starting_date }}</div>
            </div>
        </div>

    </div>
</template>

<style scoped>
.course_teachers {
    display: flex;
    gap: 10px;
}

.teacher_picture {
    background-color: #fff;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    overflow: hidden;
}

.img_course_card {
    overflow: hidden;
}

.description_course_card {
    flex: 0; 
    display: flex;
    flex-direction: column;
    padding: 0 10px 10px 10px;
    background-color: #fff;
    height: 100%;
}

.course_card {
    display: flex;
    flex-direction: column;

    max-width: 23vw;
    max-height: 40vh;
    border-radius: 25px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);

    transition: transform 0.3s;
    overflow: hidden;

    font-weight: 300;
    font-size: 0.9em;
}

.bottom_course_card {
    display: flex;
    justify-content: space-between;
}

#course_name {
    font-size: 1em;
    font-weight: 400;
}

</style>
