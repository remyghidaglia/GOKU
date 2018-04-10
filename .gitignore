#include <allegro.h>
#include <time.h>

int main()
{

    BITMAP *image;
    BITMAP *image2;
    BITMAP* image3;
    BITMAP* image4;
    BITMAP* image5;
    BITMAP* image6;
    BITMAP* image7;
    BITMAP* FOND;
    BITMAP* TAMPON;
    // Il y aura un peu de hasard...
    srand(time(NULL));

    int tx,ty;
    int posx,posy;    // coordonnées       // taille (largeur et hauteur)
    int deplacement;
    int i=0;

    // Lancer allegro et le mode graphique
    allegro_init();
    install_keyboard();

    set_color_depth(desktop_color_depth());
    if (set_gfx_mode(GFX_AUTODETECT_WINDOWED,800,600,0,0)!=0)
    {
        allegro_message("prb gfx mode");
        allegro_exit();
        exit(EXIT_FAILURE);
    }

    // Chargement de l'image (l'allocation a lieu en même temps)
    image=load_bitmap("goku se bat 2.bmp",NULL);
    image2=load_bitmap("goku se bat 1.bmp",NULL);
    image3=load_bitmap("goku au repos.bmp",NULL);
    image4=load_bitmap("goku monte.bmp",NULL);
    image5=load_bitmap("goku descend.bmp",NULL);
    image6=load_bitmap("goku avance.bmp",NULL);
    image7=load_bitmap("goku recule.bmp",NULL);
    FOND=load_bitmap("FOND.bmp",NULL);
    TAMPON=create_bitmap(SCREEN_W,SCREEN_H);

    if (!image)
    {
        allegro_message("pas pu trouver/charger mon_image.bmp");
        allegro_exit();
        exit(EXIT_FAILURE);
    }
    if (!image2)
    {
        allegro_message("pas pu trouver/charger mon_image.bmp");
        allegro_exit();
        exit(EXIT_FAILURE);
    }
    if (!image3)
    {
        allegro_message("pas pu trouver/charger mon_image.bmp");
        allegro_exit();
        exit(EXIT_FAILURE);
    }
    if (!image4)
    {
        allegro_message("pas pu trouver/charger mon_image.bmp");
        allegro_exit();
        exit(EXIT_FAILURE);
    }
    if (!image5)
    {
        allegro_message("pas pu trouver/charger mon_image.bmp");
        allegro_exit();
        exit(EXIT_FAILURE);
    }
    if (!image6)
    {
        allegro_message("pas pu trouver/charger mon_image.bmp");
        allegro_exit();
        exit(EXIT_FAILURE);
    }
    if (!image7)
    {
        allegro_message("pas pu trouver/charger mon_image.bmp");
        allegro_exit();
        exit(EXIT_FAILURE);
    }
    if (!FOND)
    {
        allegro_message("pas pu trouver/charger mon_image.bmp");
        allegro_exit();
        exit(EXIT_FAILURE);
    }


    tx=(image->w)+5;
    ty=(image->h)+5;
    posx=0;
    posy=SCREEN_H/2-ty/2;
    // Affichage de l'image sur l'écran au milieu
    deplacement=5;

    // Boucle interactive
    while (!key[KEY_ESC])
    {

        clear_bitmap(TAMPON);
        blit(FOND,TAMPON,0,0,0,0,SCREEN_W,SCREEN_H);
        draw_sprite(TAMPON,image3,posx,posy);
        {

        if (key[KEY_UP])
        {

            posy = posy-deplacement;
            clear_bitmap(TAMPON);
        blit(FOND,TAMPON,0,0,0,0,SCREEN_W,SCREEN_H);
            draw_sprite(TAMPON,image4,posx,posy);

        }

        if (key[KEY_DOWN])
        {

            posy = posy+deplacement;
            clear_bitmap(TAMPON);
        blit(FOND,TAMPON,0,0,0,0,SCREEN_W,SCREEN_H);
            draw_sprite(TAMPON,image5,posx,posy);
        }

        if (key[KEY_LEFT])
        {

            posx = posx-deplacement;
            clear_bitmap(TAMPON);
        blit(FOND,TAMPON,0,0,0,0,SCREEN_W,SCREEN_H);
            draw_sprite(TAMPON,image7,posx,posy);
        }
             // mouvement négatif en abscisses

        if (key[KEY_RIGHT])
            {

            posx = posx+deplacement;
            clear_bitmap(TAMPON);
        blit(FOND,TAMPON,0,0,0,0,SCREEN_W,SCREEN_H);
            draw_sprite(TAMPON,image6,posx,posy);
            }
        if (key[KEY_SPACE])
        {

            do
            {
            if((i%2)==0)
            {
                clear_bitmap(TAMPON);
                blit(FOND,TAMPON,0,0,0,0,SCREEN_W,SCREEN_H);
                draw_sprite(TAMPON,image,posx,posy);
                rest(20);

            }

            else

            {
                clear_bitmap(TAMPON);
                blit(FOND,TAMPON,0,0,0,0,SCREEN_W,SCREEN_H);
                draw_sprite(TAMPON,image2,posx,posy);
                rest(20);

            }
            i++;

            }while(key[KEY_ENTER]);

        }

        if (posx+tx<0) posx = SCREEN_W+posx+tx;
        if (posx>=SCREEN_W) posx = posx-SCREEN_W-tx;            //passage de haut en bas et de gauche à droite
        if (posy+ty<0) posy = SCREEN_H+posy+ty;
        if (posy>=SCREEN_H) posy = posy-SCREEN_H-ty;

        rest(5);
        }
        blit(TAMPON,screen,0,0,0,0,SCREEN_W,SCREEN_H);
    }

    return 0;
}
END_OF_MAIN();
