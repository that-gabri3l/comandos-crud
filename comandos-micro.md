# INSERTS

```sql
INSERT INTO usuarios (nome, email, senha, tipo_usario) VALUES
('Ana Silve', 'ana@email.com', '123acb', 'editor');

INSERT INTO usuarios (nome, email, senha, tipo_usario) VALUES
('Bruno Souza', 'bruno@email.com', 'abc345', 'admin');

INSERT INTO usuarios (nome, email, senha, tipo_usario) VALUES
('Carla Mendes', 'carla@email.com', '789xyz', 'editor');
```

## Categoria

```sql
    INSERT INTO categorias (nome) VALUES ('Tecnologia');
    INSERT INTO categorias (nome) VALUES ('Educação');
    INSERT INTO categorias (nome) VALUES ('Entretenimento');
```

## Noticia

```sql
INSERT INTO noticias (titulo, resumo, text_completo, imagem, destaque, usuario_id, categoria_id) VALUES ( 'Inteligência Artificial transforma a educação',
 'Ferramentas de IA estão sendo usadas em salas de aula de todo o Brasil.',
  'A inteligência artificial está mudando a forma como alunos e professores interagem com o conteúdo. Plataformas personalizadas ajudam no aprendizado individualizado e no acompanhamento do desempenho dos estudantes.',
   'ia-educacao.jpg',
    'sim',
    1,
    2 )
    (
    'Nova série de ficção científica estreia este mês',
    'Produção nacional promete revolucionar o entretenimento brasileiro.',
    'A nova série de ficção científica produzida no Brasil chega às plataformas de streaming com grande expectativa. O enredo mistura tecnologia avançada e dilemas humanos, e já recebeu elogios da crítica especializada.',
    'serie-ficcao.jpg',
    'sim',
    2,
    3
),
(
    'Lançamento de novo smartphone com recursos avançados',
    'Empresa anuncia aparelho com câmera de alta resolução e bateria de longa duração.',
    'O novo smartphone chega ao mercado brasileiro com especificações de ponta. Entre os destaques estão a tela de alta taxa de atualização, processador de última geração e sistema de câmeras inovador.',
    'smartphone-novo.jpg',
    'nao',
    3,
    1
),
(
    'Plataforma de cursos online cresce 40% em 2026',
    'Educação a distância continua em expansão no país.',
    'Uma das principais plataformas de cursos online do Brasil registrou crescimento de 40% no número de alunos este ano. Os cursos de tecnologia e programação lideram as preferências dos usuários.',
    'cursos-online.jpg',
    'nao',
    1,
    2
);
```

## Alteraçãoes no microblog 

```sql
--Nome de usuario
UPDATE  usuarios SET nome = 'Pedro Silva' WHERE id = 1
UPDATE usuarios SET nome = 'Bruna Prado' WHERE id =2
UPDATE usuarios SET nome = 'Carlos Ronaldo' WHERE id = 3
```
```sql
--Tipo de usuario
UPDATE usuarios SET tipo_usario = 'admin' WHERE id = 1
UPDATE usuarios SET tipo_usario = 'editor' WHERE id = 2

--Categoria
UPDATE categorias SET nome = 'Produção' WHERE id = 2

--titulo da noticia 
UPDATE noticias SET titulo = 'Ferramentas de IA nas Salas de aula' WHERE id = 1

-- Destaque
UPDATE noticias SET destaque = 'nao' WHERE id = 1
UPDATE noticias SET destaque = 'nao' WHERE id = 3

-- Categoria 
UPDATE noticias SET categoria_id = '2' WHERE id = 3
UPDATE noticas SET usuario_id = '2' WHERE id = 3
```
```sql
DELETE FROM noticias WHERE id = 1
DELETE FROM categorias WHERE id = 1
DELETE FROM usuarios WHERE id = 3

