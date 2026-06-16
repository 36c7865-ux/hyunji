<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>장지현 포트폴리오</title>

<style>
/* 폰트 설정 */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Pacifico&family=Montserrat:wght@400;700&display=swap');

/* 전체 기본 스타일 */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: 'Montserrat', sans-serif;
}

body {
    /* 분홍색을 빼고 차분하고 세련된 딥블루 & 네이비 그라데이션으로 변경 */
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: #fff;
    line-height: 1.6;
    overflow-x: hidden;
}

/* 공통 애니메이션 */
.fade-in {
    opacity: 0;
    transform: translateY(30px);
    animation: fadeInUp 1s forwards;
}

@keyframes fadeInUp {
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Hero Section */
.hero {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    position: relative;
    overflow: hidden;
    padding: 0 20px;
}

.hero h1 {
    font-family: 'Pacifico', cursive;
    font-size: 4rem;
    margin-bottom: 1.5rem;
    /* 글자 가독성을 위해 블루 계열 그라데이션 및 그림자 추가 */
    background: linear-gradient(to right, #00d2ff, #3a7bd5);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    filter: drop-shadow(0px 4px 8px rgba(0, 0, 0, 0.3));
}

.hero p {
    font-size: 1.6rem;
    margin-bottom: 2rem;
    color: #fff;
    /* 텍스트 가독성을 위한 그림자 처리 */
    text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
    font-weight: 700;
}

/* [수정] 카메라 일러스트(.camera) 관련 CSS는 삭제되었습니다. */

/* 섹션 공통 */
section {
    padding: 100px 20px;
    max-width: 1200px;
    margin: 0 auto;
}

section h2 {
    text-shadow: 0 2px 5px rgba(0,0,0,0.3);
}

/* About Me */
#about {
    /* 가독성을 위해 배경 투명도를 조금 더 어둡고 단단하게 조정 */
    background: rgba(0, 0, 0, 0.3);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 20px;
    padding: 50px;
    margin-bottom: 50px;
}

#about h2 {
    font-size: 2.5rem;
    margin-bottom: 20px;
    color: #00d2ff; /* 포인트 컬러 변경 */
}

#about h3 {
    margin-top: 30px;
    margin-bottom: 15px;
    color: #e0e0e0;
}

.movies, .songs {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}

.movie, .song {
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.1);
    padding: 15px 25px;
    border-radius: 15px;
    cursor: pointer;
    transition: transform 0.3s, background 0.3s;
    font-weight: 700;
}

.movie:hover, .song:hover {
    transform: scale(1.05);
    background: rgba(0, 210, 255, 0.3); /* 호버 시 블루 포인트 */
}

/* My Skills */
#skills {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 50px;
}

#skills h2 {
    font-size: 2.5rem;
    margin-bottom: 20px;
    color: #00d2ff;
}

.skill-card {
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.1);
    padding: 20px 60px;
    margin: 20px 0;
    border-radius: 20px;
    font-size: 1.5rem;
    transition: transform 0.3s, background 0.3s;
    cursor: pointer;
    font-weight: 700;
}

.skill-card:hover {
    transform: translateY(-10px);
    background: rgba(0, 210, 255, 0.3);
}

/* My Favorites */
#favorites-section {
    margin-bottom: 50px;
}

#favorites-section h2 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 30px;
    color: #00d2ff;
}

#favorites {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
}

.favorite-card {
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 15px;
    text-align: center;
    padding: 30px 20px;
    font-size: 1.5rem;
    transition: transform 0.3s, background 0.3s;
    cursor: pointer;
    font-weight: 700;
}

.favorite-card:hover {
    transform: translateY(-10px);
    background: rgba(0, 210, 255, 0.3);
}

/* Footer */
footer {
    text-align: center;
    padding: 50px 20px;
    font-size: 1rem;
    background: rgba(0,0,0,0.4);
    color: #bbb;
}

/* Typing Effect */
.typing {
    border-right: .1em solid #fff;
    white-space: nowrap;
    overflow: hidden;
}

/* 미디어쿼리 */
@media(max-width:768px){
    .hero h1 {
        font-size: 2.8rem;
    }

    .hero p {
        font-size: 1.2rem;
    }
    
    #about {
        padding: 30px 20px;
    }
}
</style>
</head>
<body>

<section class="hero fade-in">
    <h1>Hi, I'm Jihyun!</h1>
    <p>A Movie Lover & Social Thinker 🎬</p>
    </section>

<section id="about" class="fade-in">
    <h2>About Me</h2>
    <p style="font-size: 1.1rem; margin-bottom: 20px;">Hi! I'm 장지현, a bright personality who loves movies, social issues, and gaming. Let's dive into my world!</p>

    <h3>🎬 Favorite Movies</h3>
    <div class="movies">
        <div class="movie">La La Land</div>
        <div class="movie">Lady Bird</div>
        <div class="movie">Ms. Marvel</div>
        <div class="movie">Extreme Festival</div>
        <div class="movie">Phoenician Scheme</div>
        <div class="movie">Sing Street</div>
    </div>

    <h3>🎵 Favorite Song</h3>
    <div class="songs">
        <div class="song">Somber - Artist</div>
    </div>
</section>

<section id="skills" class="fade-in">
    <h2>My Skills</h2>
    <div class="skill-card">💪 노동</div>
</section>

<section id="favorites-section" class="fade-in">
    <h2>My Favorites</h2>
    <div id="favorites">
        <div class="favorite-card">🎬 Movies</div>
        <div class="favorite-card">🎵 Music</div>
        <div class="favorite-card">🎮 Gaming</div>
    </div>
</section>

<footer>
    <p>&copy; 2026 Jihyun Jang. All rights reserved.</p>
</footer>

</body>
</html>
