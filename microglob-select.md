
```sql
-- 1. Todos os dados de todos os usuários
SELECT * FROM usuarios;

-- 2. Apenas nome e e-mail 
SELECT nome, email FROM usuarios;

-- 3. Dados das categorias 
SELECT * FROM categorias;

-- 4. Apenas título e data de publicação
SELECT titulo, data_publicacao FROM noticias;

-- 5. renomear pelo menos duas colunas
SELECT titulo AS "Título da Notícia", data_publicacao AS "Publicado em", destaque AS "É destaque?" FROM noticias;

-- 6. Apenas usuários do tipo admin
SELECT * FROM usuarios WHERE tipo_usario = 'admin';

-- 7. Apenas notícias marcadas como destaque
SELECT * FROM noticias WHERE destaque = 'sim';

-- 8. Notícias da categoria Tecnologia 
SELECT * FROM noticias WHERE categoria_id = 1;

-- 9. Usando <> para excluir editores do resultado
SELECT * FROM usuarios WHERE tipo_usario <> 'editor';

-- 10. Duas condições simultâneas com AND
SELECT * FROM noticias WHERE destaque = 'sim' AND categoria_id = 4;

-- 11. Uma condição OU outra com OR
SELECT * FROM noticias WHERE categoria_id = 1 OR categoria_id = 9;

-- 12. LIKE para procurar registros que contenham uma palavra
SELECT * FROM noticias WHERE titulo LIKE '%brasileiro%';

-- 13. LIKE para registros que comecem com determinada letra/palavra
SELECT * FROM usuarios WHERE nome LIKE 'C%';

-- 14. Notícias da mais recente para a mais antiga
SELECT titulo, data_publicacao FROM noticias ORDER BY data_publicacao DESC;

-- 15. Categorias em ordem alfabética
SELECT nome FROM categorias ORDER BY nome ASC;

-- 16. Quantidade de usuários cadastrados
SELECT COUNT(*) AS total_usuarios FROM usuarios;

-- 17. Quantidade de notícias cadastradas
SELECT COUNT(*) AS total_noticias FROM noticias;

-- 18. Data da notícia mais antiga e da mais recente
SELECT MIN(data_publicacao) AS mais_antiga, MAX(data_publicacao) AS mais_recente FROM noticias;

-- 19.  "Quais notícias em destaque, das categorias Tecnologia ou Ciência, têm 'inteligência' no título, mostrando apenas título e data renomeados, das mais novas para as mais antigas?"
SELECT titulo AS "Título", data_publicacao AS "Data"
FROM noticias
WHERE destaque = 'sim'
  AND (categoria_id = 1 OR categoria_id = 9)
  AND titulo LIKE '%inteligência%'
ORDER BY data_publicacao DESC;