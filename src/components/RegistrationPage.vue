<template>
  <div class="container">
    <div class="card">
    <patient-profile-section></patient-profile-section>
    <emergency-contact-section></emergency-contact-section>
    <allergy-info-section></allergy-info-section>
    <confirm-section class="my-section"></confirm-section>
    </div>
  </div> 
</template>
<script>
import PatientProfileSection from './PatientProfileSection.vue';
import EmergencyContactSection from './EmergencyContactSection.vue';
import AllergyInfoSection from './AllergyInfoSection.vue';
import ConfirmSection from './ConfirmSection.vue';

export default {
    components: {
        PatientProfileSection,
        EmergencyContactSection,
        AllergyInfoSection,
        ConfirmSection
    }
}
</script>
<style scoped>
.section {
    position: relative;
    display: flex;
    flex-direction: column;
    border: 1px solid #ffdd57;
    border-top-right-radius: 4px;
    border-bottom-right-radius: 4px;
    border-bottom-left-radius: 4px;
    color: rgba(0,0,0,.7);
}
</style>