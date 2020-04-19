Тест
---------

.. mchoice:: Тест7_Питање1
   :answer_a: plt.plot(predmeti, ocene)
   :answer_b: plt.bar(predmeti, ocene)
   :answer_c: plt.barh(predmeti, ocene)
   :answer_d: plt.histogram(predmeti, ocene)
   :correct: b

   Библиотека `matplotlib.pyplot` је увезена у програм овако:
   
   .. code-block:: python
   
      import matplotlib.pyplot as plt
   
   Помоћу ње је нацртан следећи дијаграм:

   .. image:: test807sl1.png
      :width: 600

   Којом од понуђених наредби је дијаграм нацртан?

.. mchoice:: Тест7_Питање2
   :answer_a: plt.figsize(10, 5)
   :answer_b: plt.figsize=(10, 5)
   :answer_c: plt.figure(10, 5)
   :answer_d: plt.figure(figsize=(10, 5))
   :correct: d

   Библиотека `matplotlib.pyplot` је увезена и помоћу ње је нацртан дијаграм
   као у првом задатку. Како можемо променити димензије тог дијаграма?
   
.. mchoice:: Тест7_Питање3
   :answer_a: plt.figure(color="g")
   :answer_b: plt.plot(predmeti, ocene, color="g")
   :answer_c: plt.bar(predmeti, ocene, color="g")
   :answer_d: plt.figcolor="g"
   :correct: c

   Библиотека `matplotlib.pyplot` је увезена и помоћу ње је нацртан дијаграм
   као у првом задатку. Која команда исцртава исти дијаграм, али тако да
   стубићи буду зелени?
   
.. mchoice:: Тест7_Питање4
   :answer_a: Легенда на дијаграму је добијена употребом командe legend.
   :answer_b: Легенда на дијаграму је добијена употребом команди ylim и legend.
   :answer_c: Легенда на дијаграму је добијена употребом команде ylim и опције label.
   :answer_d: Легенда на дијаграму је добијена употребом команде legend и опције label.
   :correct: d

   Следећи дијаграм:

   .. image:: test807sl2.bmp
      :width: 600
   
   је нацртан помоћу овог програма:
   
   .. code-block:: python
      
      import matplotlib.pyplot as plt
      plt.bar(starosneGrupe, normalnaT_gornja, label="gornja granica")
      plt.bar(starosneGrupe, normalnaT_donja, label="donja granica")
      plt.ylim(34,39)
      plt.title("Normalna telesna temperatura po starosnim grupama")
      plt.xlabel("Starosne grupe (godine)")
      plt.ylabel("Temperatura (C)")
      plt.legend()
      plt.show()
      plt.close()

   Означи исказ који садржи највише тачних информација (*само један*):
