#create db
-psql
-CREATE DATABASE namadb;

#create user dan password
-psql
-CREATE ROLE nama_pengguna WITH LOGIN ENCRYPTED PASSWORD 'kata_sandi';

#permision
-psql
GRANT ALL PRIVILEGES ON SCHEMA public TO nama_pengguna;

#melihat semua role
-psql
SELECT rolname FROM pg_roles;

#melihat semua user
-psql

SELECT * FROM pg_user;


#membuat db dengan user dan password
-psql
-- Buat pengguna "dimmas" dengan kata sandi "dimmas"
CREATE USER dimmas WITH PASSWORD 'dimmas';

-- Buat database "pos" dan berikan izin kepada pengguna "dimmas"
CREATE DATABASE pos;
GRANT ALL PRIVILEGES ON DATABASE pos TO dimmas;
