<template>
  <div class="family-table">
    <h2>Family</h2>
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Relation</th>
          <th>SSN</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(member, index) in family" :key="index">
          <td>{{ member.name }}</td>
          <td>{{ member.relation }}</td>
          <td
            @mouseover="member.showFullSSN = true"
            @mouseleave="member.showFullSSN = false"
          >
            {{ member.showFullSSN ? member.ssn : maskSSN(member.ssn) }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'FamilyTable',
  data() {
    return {
      family: [
        {
          name: '양아빠',
          relation: 'Father',
          ssn: '810101-1234567',
          showFullSSN: false,
        },
        {
          name: '양엄마',
          relation: 'Mother',
          ssn: '820202-2345678',
          showFullSSN: false,
        },
        {
          name: '양태원',
          relation: 'Son',
          ssn: '040403-3456789',
          showFullSSN: false,
        },
        {
          name: '양누나',
          relation: 'Daughter',
          ssn: '050504-4567890',
          showFullSSN: false,
        },
      ],
    };
  },
  methods: {
    maskSSN(ssn) {
      return ssn.slice(0, 6) + '-*******';
    },
  },
};
</script>

<style scoped>
table {
  width: 100%;
  border-collapse: collapse;
  text-align: center;
  border: none;
}
th,
td {
  padding: 10px;
  border: 1px solid #ccc;
  border: none;
}
h2 {
  text-align: center;
}
</style>
