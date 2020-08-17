############################# 

MINILIBX DOC
============

\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#
----------------------------------------------------------

mlx\_init() //connects to x-window //and returns void ptr -- new window:
void *mlx\_new\_window ( void *mlx\_ptr, int size\_x, int size\_y, char
*title ); return NULL or non-null pointer as window identifier -\>int
mlx\_clear\_window( void *mlx\_ptr, void *win\_ptr ); -\>int
mlx\_destroy\_window( void *mlx\_ptr, void *win\_ptr ) -- pixel put: int
mlx\_pixel\_put( void *mlx\_ptr, void *win\_ptr, int x, int y, int color
); int mlx\_string\_put( void *mlx\_ptr, void *win\_ptr, int x, int y,
int color, char *string ); -\> color int = 0 + r + g + b -- image
manipulation: void *mlx\_new\_image ( void *mlx\_ptr, int width, int
height ); int mlx\_put\_image\_to\_window ( void *mlx\_ptr, void
*win\_ptr, void *img\_ptr, int x, int y ); char *mlx\_get\_data\_addr (
void *img\_ptr, int *bits\_per\_pixel, int *size\_line, int *endian );
-\> bits\_per\_pixel : bits for one pixel -\> size\_line : bits for one
line -\> endian :\
 int mlx\_destroy\_image ( void *mlx\_ptr, void *img\_ptr ); -- image
manipulation v2: unsigned int mlx\_get\_color\_value ( void *mlx\_ptr,
int color ); void *mlx\_xpm\_to\_image ( void \*mlx\_ptr, char
\*\*xpm\_data, int *width, int *height ); void
*mlx\_xpm\_file\_to\_image ( void *mlx\_ptr, char *filename, int *width,
int *height ); -- events: int mlx\_loop ( void *mlx\_ptr ); int
mlx\_key\_hook ( void *win\_ptr, int (*funct\_ptr)(), void *param ); int
mlx\_mouse\_hook ( void *win\_ptr, int (*funct\_ptr)(), void *param );
int mlx\_expose\_hook ( void *win\_ptr, int (*funct\_ptr)(), void *param
); int mlx\_loop\_hook ( void *mlx\_ptr, int (*funct\_ptr)(), void
*param ); -- compile links: -lmlx -lXext -lX11
