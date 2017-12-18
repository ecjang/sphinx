============================
Theme
============================

내장형 테마 (Bulitin Theme)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
자체적으로 제공하는 테마

스핑크스는 기본적으로 'alabaster' 테마가 적용되어 있지만 자체적으로 제공하는 다른 테마들이 있다. `관련 홈페이지 <http://www.sphinx-doc.org/en/stable/theming.html>`_ 에서 확인 할 수 있다.

.. note:: 
	- 스핑크스 홈페이지 : http://www.sphinx-doc.org/en/stable/theming.html 
	
.. image:: image/theme.png

conf.py 파일을 편집기로 열고 ``html_theme`` 를 검색하여 원하는 테마로 수정하면 적용됨.


.. literalinclude:: ./conf.py
	:linenos:
	:language: python	
	:lines: 85-90
	:emphasize-lines: 5
	
	
사용자 정의 테마 (Creating Theme)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
다른 사용자가 제작한 테마를 다운받아 사용. ``sphinx theme``를 검색하면 다양한 스핑크스 테마를 검색 가능.

.. note:: 
	- 스핑크스 테마 모음 : http://www.writethedocs.org/guide/tools/sphinx-themes/ 

.. image:: image/theme2.png

pip 명령어로 해당 테마를 설치한 후 conf.py에서 다운 받은 테마를 지정해서 적용하는 방식.

.. note::
	- sphinx_bootstrap_theme 테마 설치 시
	- 테마 설치 :  pip install sphinx_bootstrap_theme
	- 테마 적용 : conf.py 파일을 수정
	- 상단에 ``import sphinx_bootstrap_theme``
	- 중간부분에 ``html_theme = 'bootstrap'``
	- 중간부분에 ``html_theme_path = sphinx_bootstrap_theme.get_html_theme_path()``