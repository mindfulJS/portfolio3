<svg width="1440px" height="204px" viewBox="0 0 1440 204" version="1.1" class="w-full h-full">
	<defs>
		<filter x="-50%" y="-50%" width="200%" height="200%" filterUnits="objectBoundingBox" id="filter-1">
			<feOffset dx="0" dy="-4" in="SourceAlpha" result="shadowOffsetOuter1"></feOffset>
			<feGaussianBlur stdDeviation="0" in="shadowOffsetOuter1" result="shadowBlurOuter1"></feGaussianBlur>
			<feColorMatrix values="0 0 0 0 0   0 0 0 0 0   0 0 0 0 0  0 0 0 0.056 0" in="shadowBlurOuter1" type="matrix" result="shadowMatrixOuter1"></feColorMatrix>
			<feMerge>
				<feMergeNode in="shadowMatrixOuter1"></feMergeNode>
				<feMergeNode in="SourceGraphic"></feMergeNode>
			</feMerge>
		</filter>
	</defs>
	<path d="M6.05022984e-08,204 C0.00535896441,203.997351 356.00274,28.000572 720,104 C1084,180 1440,4 1440,4 L0,4 L0,204 L0,4 L1440,4 L1440,204 L0,204 Z"
	 fill="white" filter="url(#filter-1)"></path>
</svg>