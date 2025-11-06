---
layout: page
title: "Skills and Coursework"
permalink: /skills/
author_profile: true
---

<style>
/* Minimal local styles so the toggles look neat with existing theme */
.skills-cats { display:flex; flex-wrap:wrap; gap:12px; margin-bottom:18px; }
.skills-cat { cursor:pointer; padding:10px 14px; border:1px solid #e0d7d0; border-radius:4px; background:#fff6f2; font-weight:600; }
.skills-cat.active { background:#e8b7b0; color:#fff; }
.skills-list { margin:12px 0 24px 0; display:none; }
.skills-list ul { list-style:none; padding:0; margin:6px 0; }
.skills-list li { display:inline-block; margin:6px 8px 6px 0; padding:8px 12px; background:#f1e6e2; border-radius:4px; }
.courses { margin-top:28px; }
.course-item { margin:6px 0; padding:8px 10px; background:#fff2ee; border-radius:4px; }
</style>

<div class="skills-page">

<h2>Skills</h2>

<div class="skills-cats" role="tablist" aria-label="Skill categories">
	<div class="skills-cat" data-target="languages">Languages</div>
	<div class="skills-cat" data-target="frameworks">Frameworks</div>
	<div class="skills-cat" data-target="data-modeling">Data Modeling</div>
	<div class="skills-cat" data-target="devops">DevOps</div>
</div>

<div id="languages" class="skills-list" role="tabpanel">
	<ul>
		<li>Python</li>
		<li>Java</li>
		<li>SQL</li>
		<li>C</li>
		<li>C++</li>
		<li>Bash</li>
	</ul>
</div>

<div id="frameworks" class="skills-list" role="tabpanel">
	<ul>
		<li>Pandas</li>
		<li>PySpark</li>
		<li>PyTorch</li>
		<li>PyCUDA</li>
		<li>Scikit-learn</li>
		<li>LangChain</li>
		<li>Hugging Face</li>
		<li>Streamlit</li>
		<li>Boto3</li>
		<li>FastAPI</li>
	</ul>
</div>

<div id="data-modeling" class="skills-list" role="tabpanel">
	<ul>
		<li>Dremio</li>
		<li>Apache Iceberg</li>
		<li>SQLite</li>
		<li>DuckDB</li>
		<li>MongoDB</li>
		<li>PostgreSQL</li>
		<li>Redis</li>
	</ul>
</div>

<div id="devops" class="skills-list" role="tabpanel">
	<ul>
		<li>Git</li>
		<li>Docker</li>
		<li>Kubernetes</li>
		<li>Helm Charts</li>
		<li>Jira</li>
		<li>Confluence</li>
		<li>MLflow</li>
	</ul>
</div>

<div class="courses">
	<h3>Selected Coursework</h3>
	<div class="course-item">Intro to LLMs and Generative AI</div>
	<div class="course-item">Machine Learning</div>
	<div class="course-item">Causal Inference</div>
	<div class="course-item">Predictive Analytics</div>
	<div class="course-item">Data Management and Analysis</div>
	<div class="course-item">Natural Language Processing</div>
	<div class="course-item">Parallel Computing</div>
	<div class="course-item">Data Structures and Algorithms</div>
	<div class="course-item">Linear Algebra</div>
	<div class="course-item">Mathematics of Finance</div>
</div>

</div>

<script>
// Simple toggle logic: click a category to show its skills and hide others
document.addEventListener('DOMContentLoaded', function () {
	const cats = Array.from(document.querySelectorAll('.skills-cat'));
	const lists = Array.from(document.querySelectorAll('.skills-list'));

	function clearActive() {
		cats.forEach(c => c.classList.remove('active'));
		lists.forEach(l => l.style.display = 'none');
	}

	cats.forEach(cat => {
		cat.addEventListener('click', function () {
			const target = this.dataset.target;
			const el = document.getElementById(target);
			if (!el) return;
			const isVisible = el.style.display === 'block';
			clearActive();
			if (!isVisible) {
				this.classList.add('active');
				el.style.display = 'block';
			}
		});
	});

	// Optionally activate the first category on load
	if (cats.length) cats[0].click();
});
</script>

