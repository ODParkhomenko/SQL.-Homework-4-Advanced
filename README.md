# SQL.-Homework-4-Advanced

Select genre_name count(id_artist) from Genres 
Join Artists_Genres on Genres.id_genre=Artists_Genres.id_genre_ag



Select count(album_name) from Tracks

join albums on Tracks.id_album_t = Albums.id_album

where album_release_year >= '20190101' and album_release_year <= '20201231'


select album_name, avg(track_duration) from Tracks

join Albums on Tracks.id_album_t = Albums.id_album

group by album_name



select artist_name from Artists
join Artists_Album on Artists.id_artist = Artists_Album.id_artist_aa
join Albums on Albums.id_album = Artists_Album.id_album_aa
where album_release_year not between '20200101' and '20201231'
group by artist_name




select collection_title from Collections

join Collection_Tracks on Collection_Tracks.id_collection_ct = Collections.id_collection

join Tracks on Collection_Tracks.id_track_ct = Tracks.id_track

join Albums on Tracks.id_album_t = Albums.id_album

join Artists_Album on Artists_Album.id_album_aa = Albums.id_album

join Artists on Artists_Album.id_artist_aa =  Artists.id_artist

where artist_name = 'Taylor Swift'

group by collection_title
