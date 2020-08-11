PREFIX_PKG := django_tutorial_polls


default:
	grep -E ':\s+#' Makefile

run-dev:
	python manage.py runserver 8001

run-prod:
	python manage.py runserver 8000

	
deploy:
	rm -rf dist $(PREFIX_PKG)*
	rm -rf polls.dist
	cd polls && python setup.py sdist
	mkdir polls.dist && mv polls/dist/* polls/$(PREFIX_PKG)* polls.dist
