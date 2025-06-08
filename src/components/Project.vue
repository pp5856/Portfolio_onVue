<template>
  <div>
    <h2>Project</h2>
    <!-- 
         ProjectItem 컴포넌트를 사용하여 프로젝트 항목을 표시합니다. 
        v-for 디렉티브를 사용하여 projects의 각 항목에 대해 반복하고,
         :key로 index를 부여합니다. 
         :project로 각 프로젝트 데이터를 전달합니다.
         -->
    <ProjectItem
      v-for="(item, index) in projects"
      :key="index"
      :project="item"
    />
  </div>
</template>

<script>
// ProjectItem.vue 컴포넌트를 import합니다.
import ProjectItem from './ProjectItem.vue';

export default {
  name: 'ProjectList',
  // 사용하는 컴포넌트를 등록합니다. ProjectItem 컴포넌트를 사용합니다.
  components: {
    ProjectItem,
  },
  data() {
    return {
      // 사용자의 프로젝트 정보 리스트를 저장합니다.
      projects: [
        {
          title: 'Awoolim 프로젝트',
          items: [
            'Svelte, Electron.js 기반 데스크탑 건강관리 프로젝트',
            'TF Lite를 이용한 웹캠기반 자세 분석 피드백',
            'Gemini Api를 이용한 사용자 맞춤형 자연어 피드백',
          ],
        },
        {
          title: 'Fall-In-One 프로젝트',
          items: [
            '한국 대학교의 외국인 학생을 위한 구직 서비스',
            '대학교 인근 자영업 사장님들과 협업하여 저렴한 노동력 제공을 혜택으로 일자리를 구하기 힘든 외국인 학생들에게 일자리 제공',
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
div {
  text-align: left;
}
</style>
