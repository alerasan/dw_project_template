# DWM100x project template

### This is project template with systemview and rtt logging features for all DecaWave tags/nodes except ttk-1000

Simply add (or ever symlink) your projects to examples folder and decawave driver folder to root folder

You main.c may contain code like this after initialization, but before scheduling:

`
    /* USER CODE BEGIN RTOS_MUTEX */

    sysview_all_irq_log(true);

    //sysview_irq_log( SWI2_IRQn, true );

    //sysview_irq_log( RADIO_IRQn, true );

    //sysview_irq_log( RTC1_IRQn, true );

    //sysview_irq_log( SVCall_IRQn, true );

    sysview_softdevice_enable( true, true);

    sysview_softdevice_mark_sleep(true);

    SEGGER_SYSVIEW_Conf();

    /* USER CODE END RTOS_MUTEX */

    SEGGER_SYSVIEW_Print("egor");

    /* USER CODE BEGIN RTOS_SEMAPHORES */
`

Regards

