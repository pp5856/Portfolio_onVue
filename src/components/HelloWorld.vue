<template>
  <div id="app">
    <NameCard></NameCard>
    <AboutMe></AboutMe>
    <Info></Info>
    <ConTact></ConTact>
    <EduCation></EduCation>
    <Project></Project>
    <hr />
    <FamilyTable></FamilyTable>
  </div>
</template>

<script>
// 포트폴리오 제목 컴포넌트
import NameCard from './NameCard.vue';
// 자기 소개 컴포넌트
import AboutMe from './AboutMe.vue';
// 정보 컴포넌트
import Info from './Info.vue';
// 연락처 컴포넌트
import ConTact from './ConTact.vue';
// 학교 정보 컴포넌트
import EduCation from './EduCation.vue';
// 프로젝트 컴포넌트
import Project from './Project.vue';

import FamilyTable from './FamilyTable.vue';

export default {
  name: 'App',
  components: {
    NameCard,
    Info,
    ConTact,
    AboutMe,
    EduCation,
    Project,
    FamilyTable,
  },
};
</script>
