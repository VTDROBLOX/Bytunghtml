<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hồ Sơ Cá Nhân - Nguyễn Văn A</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }

        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid white;
            margin: 0 auto 20px;
            display: block;
            object-fit: cover;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        .header p {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .content {
            padding: 40px;
        }

        .section {
            margin-bottom: 30px;
        }

        .section-title {
            font-size: 1.8em;
            color: #667eea;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 3px solid #667eea;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .info-item {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }

        .info-label {
            font-weight: bold;
            color: #667eea;
            margin-bottom: 5px;
        }

        .info-value {
            color: #333;
            font-size: 1.1em;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .skill-tag {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            font-size: 0.9em;
        }

        .timeline {
            position: relative;
            padding-left: 30px;
            margin-top: 20px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 3px;
            background: #667eea;
        }

        .timeline-item {
            position: relative;
            margin-bottom: 30px;
            padding-left: 20px;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -36px;
            top: 5px;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            background: #667eea;
            border: 3px solid white;
            box-shadow: 0 0 0 3px #667eea;
        }

        .timeline-date {
            color: #667eea;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .timeline-title {
            font-size: 1.2em;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .timeline-description {
            color: #666;
        }

        .contact-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .contact-link {
            display: inline-block;
            padding: 12px 25px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .contact-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.4);
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 2em;
            }

            .content {
                padding: 20px;
            }

            .info-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <img src="https://via.placeholder.com/150" alt="Ảnh đại diện" class="profile-image">
            <h1>Nguyễn Văn A</h1>
            <p>Nhà Phát Triển Web Full-Stack</p>
        </div>

        <div class="content">
            <div class="section">
                <h2 class="section-title">📋 Thông Tin Cá Nhân</h2>
                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-label">📧 Email</div>
                        <div class="info-value">nguyenvana@email.com</div>
                    </div>
                    <div class="info-item">
                        <div class="info-label">📱 Điện thoại</div>
                        <div class="info-value">+84 123 456 789</div>
                    </div>
                    <div class="info-item">
                        <div class="info-label">📍 Địa chỉ</div>
                        <div class="info-value">Hà Nội, Việt Nam</div>
                    </div>
                    <div class="info-item">
                        <div class="info-label">🎂 Ngày sinh</div>
                        <div class="info-value">01/01/1995</div>
                    </div>
                </div>
            </div>

            <div class="section">
                <h2 class="section-title">💼 Giới Thiệu</h2>
                <p style="line-height: 1.8; color: #555;">
                    Tôi là một lập trình viên Full-Stack với hơn 5 năm kinh nghiệm trong việc phát triển các ứng dụng web 
                    và mobile. Đam mê công nghệ và luôn tìm kiếm những giải pháp sáng tạo để giải quyết các vấn đề phức tạp. 
                    Có kinh nghiệm làm việc với nhiều công nghệ hiện đại và khả năng làm việc nhóm tốt.
                </p>
            </div>

            <div class="section">
                <h2 class="section-title">🎓 Học Vấn</h2>
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-date">2013 - 2017</div>
                        <div class="timeline-title">Cử nhân Khoa học Máy tính</div>
                        <div class="timeline-description">Đại học Bách Khoa Hà Nội - GPA: 3.6/4.0</div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-date">2017 - 2019</div>
                        <div class="timeline-title">Thạc sĩ Công nghệ Thông tin</div>
                        <div class="timeline-description">Đại học Quốc Gia Hà Nội - GPA: 3.8/4.0</div>
                    </div>
                </div>
            </div>

            <div class="section">
                <h2 class="section-title">💼 Kinh Nghiệm Làm Việc</h2>
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-date">2019 - 2021</div>
                        <div class="timeline-title">Junior Developer - Công ty ABC Tech</div>
                        <div class="timeline-description">
                            Phát triển và bảo trì các ứng dụng web sử dụng React và Node.js. 
                            Tham gia xây dựng hệ thống quản lý nội bộ cho công ty.
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-date">2021 - Hiện tại</div>
                        <div class="timeline-title">Senior Developer - Công ty XYZ Solutions</div>
                        <div class="timeline-description">
                            Lãnh đạo nhóm phát triển các dự án lớn, tư vấn kiến trúc hệ thống và 
                            hướng dẫn các thành viên mới. Chuyên về microservices và cloud computing.
                        </div>
                    </div>
                </div>
            </div>

            <div class="section">
                <h2 class="section-title">🛠️ Kỹ Năng</h2>
                <div class="skills">
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">React</span>
                    <span class="skill-tag">Node.js</span>
                    <span class="skill-tag">Python</span>
                    <span class="skill-tag">MongoDB</span>
                    <span class="skill-tag">PostgreSQL</span>
                    <span class="skill-tag">Docker</span>
                    <span class="skill-tag">AWS</span>
                    <span class="skill-tag">Git</span>
                    <span class="skill-tag">Agile/Scrum</span>
                </div>
            </div>

            <div class="section">
                <h2 class="section-title">🔗 Liên Hệ</h2>
                <div class="contact-links">
                    <a href="mailto:nguyenvana@email.com" class="contact-link">📧 Email</a>
                    <a href="https://linkedin.com" class="contact-link" target="_blank">💼 LinkedIn</a>
                    <a href="https://github.com" class="contact-link" target="_blank">💻 GitHub</a>
                    <a href="tel:+84123456789" class="contact-link">📱 Gọi điện</a>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
