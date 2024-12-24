# DataLiteracy_Night
(산대특)디지털 업무전환을 위한 데이터 리터러시 입문과정     
기간 : 2024-11-26 ~ 2025-01-16      
연락처 : kennysy@naver.com

# 한글 폰트 문제 해결

        # 한글 폰트 문제 해결 
        # matplotlib은 한글 폰트를 지원하지 않음
        !sudo apt-get install -y fonts-nanum
        !sudo fc-cache -fv
        !rm ~/.cache/matplotlib -rf
        
        import matplotlib.pyplot as plt
        import matplotlib.font_manager as fm
        
        font_path = '/usr/share/fonts/truetype/nanum/NanumGothic.ttf'
        font_name = fm.FontProperties(fname=font_path).get_name()
        plt.rc('font', family=font_name)
