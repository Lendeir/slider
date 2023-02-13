<div class="cards">
	<div class="card">
		<img
			class="card-image"
			src="https://www.tadviser.ru/images/2/22/%D0%A2%D0%B0%D1%82%D0%BD%D0%B5%D1%84%D1%82%D1%8C_%D0%BB%D0%BE%D0%B3%D0%BE.png"
			alt="icon"
		/>
		<p class="card-text">
			Благодаря внедрению системы Test IT удалось на 40% сократить сроки тестирования за счет
			оптимизации времени на создание и обновление тестовой документации.
		</p>
		<img
			class="worker-image"
			src="https://www.tadviser.ru/images/2/22/%D0%A2%D0%B0%D1%82%D0%BD%D0%B5%D1%84%D1%82%D1%8C_%D0%BB%D0%BE%D0%B3%D0%BE.png"
			alt="worker"
		/>
		<h3>Мария Каприз</h3>
		<p class="worker-text">
			Зам. руководителя блока обеспечения и контроля качества выпуска изменений ПО "РСХБ-Интех"
		</p>
		<button class="button">Подробнее</button>
	</div>
	<div class="card">
		<img
			class="card-image"
			src="https://www.tadviser.ru/images/2/22/%D0%A2%D0%B0%D1%82%D0%BD%D0%B5%D1%84%D1%82%D1%8C_%D0%BB%D0%BE%D0%B3%D0%BE.png"
			alt="icon"
		/>
		<p class="card-text">
			Благодаря внедрению системы Test IT удалось на 40% сократить сроки тестирования за счет
			оптимизации времени на создание и обновление тестовой документации.
		</p>
		<img
			class="worker-image"
			src="https://www.tadviser.ru/images/2/22/%D0%A2%D0%B0%D1%82%D0%BD%D0%B5%D1%84%D1%82%D1%8C_%D0%BB%D0%BE%D0%B3%D0%BE.png"
			alt="worker"
		/>
		<h3>Мария Каприз</h3>
		<p class="worker-text">
			Зам. руководителя блока обеспечения и контроля качества выпуска изменений ПО "РСХБ-Интех"
		</p>
		<button class="button">Подробнее</button>
	</div>
	<div class="card">
		<img
			class="card-image"
			src="https://www.tadviser.ru/images/2/22/%D0%A2%D0%B0%D1%82%D0%BD%D0%B5%D1%84%D1%82%D1%8C_%D0%BB%D0%BE%D0%B3%D0%BE.png"
			alt="icon"
		/>
		<p class="card-text">
			Благодаря внедрению системы Test IT удалось на 40% сократить сроки тестирования за счет
			оптимизации времени на создание и обновление тестовой документации.
		</p>
		<img
			class="worker-image"
			src="https://www.tadviser.ru/images/2/22/%D0%A2%D0%B0%D1%82%D0%BD%D0%B5%D1%84%D1%82%D1%8C_%D0%BB%D0%BE%D0%B3%D0%BE.png"
			alt="worker"
		/>
		<h3>Мария Каприз</h3>
		<p class="worker-text">
			Зам. руководителя блока обеспечения и контроля качества выпуска изменений ПО "РСХБ-Интех"
		</p>
		<button class="button">Подробнее</button>
	</div>
</div>

<style>
	.card {
		grid-template-areas:
			'i i i'
			'b b b'
			'c h h'
			'c p p'
			'k k k';
	}
	.card-image {
		grid-area: i;
		width: 30vh;
	}
	.card-text {
		grid-area: b;
	}
	.worker-image {
		grid-area: c;
		width: 5vh;
		height: auto;
	}
	h3 {
		grid-area: h;
	}
	.worker-text {
		grid-area: p;
	}
	.button {
		grid-area: k;
	}
	.cards {
		display: grid;
		grid-template-columns: 1fr 1fr;
	}
	@media only screen and (max-width: 600px) {
		.cards {
			display: grid;
			grid-template-columns: 1fr;
		}
	}
</style>
