<script setup>
import { ref } from 'vue'

const mainContributors = [
  'බැඳිරැක්කේ සුදිත හිමි',
  'DR චන්ද්‍රිකා ද සිල්වා (මාදිවෙල)',
  'සීතා රංජනී මහත්මිය (මහරගම)',
  'තුෂාරි ලොකුසූරියගේ (හෝමාගම)',
  'ශානිකා හේරත් (මහව)',
  'අනිල්කා මහත්මිය (Australia)'
]

const sponsors = [
  'ප්‍රේමා පණ්ඩිතරත්න (බටුවන්දර)',
  'අමිල මහතා (මාදම්පේ)',
  'අනුලා මහත්මිය (මාදම්පේ)',
  'මෝහන් මහතා (පිළියන්දල)',
  'අයෝමි මහත්මිය (පානදුර)',
  'කුමුදුමාලී (හලාවත)',
  'ධම්මිකා මහත්මිය (පිළියන්දල)',
  'දේවිකා රාජපක්ෂ (ගම්පහ)',
  'සුනාලි චතුරිකා මහත්මිය (මාදම්පේ)',
  'මිහිඳු පුතා / යමුනා මහත්මිය (පිළියන්දල)',
  'හංසිකා (ඇල්පිටිය)',
  'සෙව්වන්දි (ඇල්පිටිය)',
  'රුවන් මහතා (පිළියන්දල)',
  'කුමුදු තුෂාරි කන්ඳගේ මහත්මිය (බටුවන්දර)',
  'නිසල් ගුණතිලක (මහරගම)',
  'ප්‍රභාත් නිරෝෂන් පෙරේරා (ගම්පහ)',
  'චම්මි මනම්පේරි (දයනි / තරංගසිංහ දෙමාපියන්ට පිං පිණිස, පිළියන්දල)',
  'තිළිණි පබළු තරූෂා (ඕස්ට්‍රේලියාව)',
  'දුල්ජා / රෝෂිත ගමගේ (ගාල්ල)',
  'දසුන් මේනක (දන්කොටුව)',
  'රේණුකා කෝදාගොඩ (ගාල්ල)',
  'ධනුෂ්ක (ගාල්ල)',
  'මොහාන් ආටිගල',
  'නාමල් / රසාංගි / තේජක / සදෙව් (මාදම්පේ)',
  'සචිනි (බේරුවල)',
  'ගුණසීලි වන්නිආරච්චි (බටුවන්දර)',
  'ගුණසීලි ජයසිංහ (බටුවන්දර)',
  'සුමිත් දිසානායක (කොළඹ)',
  'යුරේෂා (මාතර)',
  'අමා හේරත් (මහව)',
  'චමරි (රත්නපුර)',
  'තීක්ෂණ ප්‍රසාද් (මාදම්පේ)'
]

const programs = [
  {
    date: '2026/03/21',
    description: 'අම්පාර දිස්ත්‍රික්කයේ මහඔය කොට්ඨාශයට අයත්, <strong>අම්/මහ/බැඳිරැක්ක විදුහලේ</strong> ඉගෙනුම ලබන සිසුන් සඳහා අවුරුදු උත්සවයක් පැවැත්වීම සහ පාසල් උපකරණ ප්‍රදානය කිරීම.'
  },
  {
    date: '2026/03/22',
    description: 'අනුරාධපුර දිස්ත්‍රික්කයේ හබරණ පුවක්පිටිය ග්‍රාමයේ <strong>ශ්‍රී බෝධිරාජ දහම් පාසලේ</strong> ඉගෙනුම ලබන දරුවන්ට සුදු රෙදි හා පොත් ප්‍රදානය කිරීම.'
  }
]
</script>

<template>
  <main>
    <div class="content-wrapper">
      
      <!-- Hero Card -->
      <header class="section-card hero-card">
        <img src="./assets/ngo.png" alt="Logo" class="hero-logo" />
        <h1 class="hero-title sinhala-heading">සුව දිවිය සමාජ සත්කාර පදනම</h1>
        <h2 class="hero-subtitle">පින්වත් දායකත්වය ලබා දුන් පිරිසට උපහාරයක් වේවා!</h2>
        <p class="hero-desc">
          සුව දිවිය සමාජ සත්කාර පදනමේ අනුග්‍රහයෙන් පවත්වනු ලබන පුණ්‍ය මහෝත්සවයන් දෙකක් 
          වෙනුවෙන් නන් අයුරින් උපකාර කළ පින්වත් දායක පිරිස වෙත අපගේ ප්‍රණාමය මෙසේ පුද කරමු.
        </p>
      </header>
      <!-- Hosting Programs -->
      <section class="section-card">
        <h2 class="section-title sinhala-heading">
          <span>✨</span> සත්කාරක වැඩසටහන්
        </h2>
        <div class="program-list">
          <div v-for="prog in programs" :key="prog.date" class="program-item">
            <div class="program-date">{{ prog.date }}</div>
            <div class="program-details" v-html="prog.description"></div>
          </div>
        </div>
      </section>

      <!-- Contributors -->
      <section class="section-card">
        <h2 class="section-title sinhala-heading">
          <span>🌟</span> ගෞරවනීය දායක පිරිස
        </h2>
        
        <h3 class="mb-3 sinhala-heading text-accent">මූලික දායකත්වය</h3>
        <div class="contributors-grid mb-4">
          <div v-for="person in mainContributors" :key="person" class="contributor-item main">
            {{ person }}
          </div>
        </div>

        <h3 class="mt-4 mb-3 sinhala-heading text-primary">අනුග්‍රහක පිරිස</h3>
        <div class="contributors-grid">
          <div v-for="person in sponsors" :key="person" class="contributor-item">
            {{ person }}
          </div>
        </div>
      </section>

    </div>

    <!-- Footer -->
    <footer class="footer">
      <h2 class="sinhala-heading">සුව දිවිය සමාජ සත්කාර පදනම</h2>
      <p>වැඩිදුර විස්තර සඳහා විමසන්න</p>
      <div class="footer-contact">0777 102 801</div>
    </footer>
  </main>
</template>
